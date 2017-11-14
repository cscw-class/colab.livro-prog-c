# Capítulo 8: Matrizes Dinâmicas

###### Por Jordan Mendonça Costa



#### Alocação Dinâmica de Matrizes

 A alocação dinâmica de memória para matrizes é realizada da mesma forma que para vetores, com a diferença que teremos um ponteiro apontando para outro ponteiro que aponta para o valor final, ou seja é um ponteiro para ponteiro, o que é denominado 

indireção múltipla

. A indireção múltipla pode ser levada a qualquer dimensão desejada, mas raramente é necessário mais de um ponteiro para um ponteiro. Um exemplo de implementação para matriz real bidimensional é fornecido a seguir. A estrutura de dados utilizada neste exemplo é composta por um vetor de ponteiros \(correspondendo ao primeiro índice da matriz\), sendo que cada ponteiro aponta para o início de uma linha da matriz.

```cpp
#include <stdio.h>
#include <stdlib.h>

float **Alocar_matriz_real (int m, int n)
{
  float **v;  /* ponteiro para a matriz */
  int   i;    /* variavel auxiliar      */
  if (m < 1 || n < 1) { /* verifica parametros recebidos */
     printf ("** Erro: Parametro invalido **\n");
     return (NULL);
     }
  /* aloca as linhas da matriz */
  v = (float **) calloc (m, sizeof(float *));	/ Um vetor de m ponteiros para float */
  if (v == NULL) {
     printf ("** Erro: Memoria Insuficiente **");
     return (NULL);
     }
  /* aloca as colunas da matriz */
  for ( i = 0; i < m; i++ ) {
      v[i] = (float*) calloc (n, sizeof(float));	/* m vetores de n floats */
      if (v[i] == NULL) {
         printf ("** Erro: Memoria Insuficiente **");
         return (NULL);
         }
      }
  return (v); /* retorna o ponteiro para a matriz */
}

float **Liberar_matriz_real (int m, int n, float **v)
{
  int  i;  /* variavel auxiliar */
  if (v == NULL) return (NULL);
  if (m < 1 || n < 1) {  /* verifica parametros recebidos */
     printf ("** Erro: Parametro invalido **\n");
     return (v);
     }
  for (i=0; i<m; i++) free (v[i]); /* libera as linhas da matriz */
  free (v);      /* libera a matriz (vetor de ponteiros) */
  return (NULL); /* retorna um ponteiro nulo */
}

void main (void)
{
  float **mat;  /* matriz a ser alocada */
  int   l, c;   /* numero de linhas e colunas da matriz */
  int i, j;
  ...           /* outros comandos, inclusive inicializacao para l e c */
  mat = Alocar_matriz_real (l, c);

  for (i = 0; i < l; i++)
     for ( j = 0; j < c; j++)
	mat[i][j] = i+j;
  
  ...           /* outros comandos utilizando mat[][] normalmente */
  mat = Liberar_matriz_real (l, c, mat);
  ...
```

#### Alocacando cada Linha

 A técnica que parece ser a mais popular é alocar um vetor de ponteiros e depois alocar uma linha da matriz para cada ponteiro deste vetor:

```cpp
int main(int, char **)
{
    int nlinhas = 5;
    int ncol = 5;
    int **mat = new int*[nlinhas];
 
    for(int i = 0;i < nlinhas; ++i)
        mat[i] = new int[ncol];
 
    //iniciando ela com zero
    for(int i = 0;i < nlinhas; ++i)
        for(int j = 0;j < ncol; ++j)
            mat[i][j] = 0;
 
    //liberar memória
    for(int i = 0;i < nlinhas; ++i)
        delete []mat[i];
 
    delete []mat;     
 
    return 0;
}
```

O problema dessa técnica é o grande desperdício de espaço e tempo que ela gera. O desempenho desta é o pior, principalmente pelo fato de serem necessárias varias alocações e alocações de memória em C/C++ são operações que costumam ser bem caras.

Mesmo ignorando o tempo de criação da matriz, o uso dela também vai ser comprometido devido a possibilidade de cada linha dela estar numa região de memória diferente e é bem provável que o cache do processador tenha dificuldades em se manter atualizado por causa disso.

Já o desperdício de espaço ocorre devido a necessidade de se realizar varias alocações e é comum cada alocação precisa alocar um pouco mais de espaço do que o requisitado para a estrutura de controle usada internamente para gerenciar a memória.

A única vantagem em utilizar este método é quando precisamos de uma matriz absurdamente grande e alocamos cada linha apenas quando existe necessidade, mas mesmo nesse caso acredito que existam técnicas melhores para se implementar uma matriz esparsa.

#### Usar apenas um Vetor

 Uma maneira mais simples de se implementar uma matriz é utilizando apenas um vetor e realizar o acesso dos elementos como se fossem uma matriz:

```cpp
int main(int, char **)
{
    int nlinhas = 5;
    int ncol = 3;
 
    //alocando a "matriz"
    int *mat = new int[nlinhas * ncol];
 
    //colocando 5 na linha 3, coluna 2
    mat[3 * ncol + 2] = 5;
 
    //liberando a memoria
    delete []mat;
 
    return 0;
}
```

Note como o código nesse caso é muito mais simples que o anterior, o único incomodo deste código é a necessidade de armazenar o tamanho da matriz \(o número de linhas para ser mais preciso\) e ficar passando ele como parâmetro a todo momento na hora de acessar um elemento, mas não é nada complicado criar uma classe para encapsular isso.

Para acessar um elemento usamos a fórmula: elem\[linha \* ncol + col\], onde linha é o numero da linha que se quer acessar, ncol o número de colunas da matriz e col o número da coluna que se deseja acessar.

Como é feita apenas uma alocação é usado o minimo de memória possível, além de deixar o cache feliz na hora de acessar os dados.

#### Utilizando std::vector

 Por fim, podemos utilizar o std::vector e não precisamos assim nos preocupar mais em gerenciar a memória da matriz e deixar o programa mais alinhado:

```cpp
#include <iostream>
#include <vector>
 
int main(int, char **)
{
    int ncol = 4;
    int nlinha = 3;
 
    std::vector mat(ncol * nlinha);
 
    //acessando elemento 2, 1 (linha 2, coluna 1)
    mat[2 * nlinha + 1] = -1;
 
    std::cout << mat[2 * nlinha + 0] << std::endl;
    std::cout << mat[2 * nlinha + 1] << std::endl;
 
    return 0;
}
```

 Esse código é muito semelhante ao anterior, mas as operações de gerenciamento de memória foram encapsuladas com o uso de um std::vector, utilizando-se uma boa implementação de std::vector não deve existir diferença alguma de performance e uma diferença minima de consumo de memória entre este exemplo e o anterior.



#### Exercícios







