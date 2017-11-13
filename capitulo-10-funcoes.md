# Capítulo 10 - Funções

**10.1  - Definição de Função**

Uma função nada mais é do que uma subrotina usada em um programa.

Na linguagem C, denominamos função a um conjunto de comandos que realiza uma tarefa específica em um módulo dependente de código.

A função é referenciada pelo programa principal através do nome atribuído a ela.

A utilização de funções visa modularizar um programa, o que é muito comum em programação estruturada.

Desta forma podemos dividir um programa em várias partes, no qual cada função realiza uma tarefa bem definida.

Esqueleto de uma função: 

```
tipo_de_retorno nome_da_função (listagem de parâmetros)
{
   instruções;
   retorno_da_função;
}
```

**10.2 - Parâmetros de uma função**

Os parâmetros são as variáveis declaradas diretamente no cabeçalho da função.

A finalidade dos parâmetros é fazer a comunicação entre as funções e a função principal.

Chamamos de passagem de parâmetros a passagem de valores entre as funções.

**Exemplo de programa usando função em C:**

```c
#include<stdio.h>
#include<conio.h>
/**

   Nome da função: multiplica
   recebe como parâmetos dois valores inteiros (N1,N2)
   objetivo:  multiplicar os valores recebidos nos parâmetros.
   retorno:  um parâmetro inteiro (res) contendo o resultado
**/
int multiplica(int N1, int N2) //multiplica recebe N1,N2 e retorna um int
{
  int resultado;
  resultado = N1 * N2;
  return(resultado); //retornando o valor para main
}

/******************* função principal (main) *********************/

int main(void)
{
  int V1, V2, resultado;
  printf("Digite o primeiro valor:");
  scanf("%d", &V1);
  printf("Digite o segundo valor:");
  scanf("%d", &V2);

  //chama a função e recebe o retorno
  resultado = multiplica(V1,V2);
  printf("Resultado = %d\n", resultado);
  getch();
  return 0;
}
```

**Explicação do código do programa:**

Observe que o corpo da função multiplica foi declarado e a implementação do código foi feita antes da função main.

Na função main os valores de V1 e V2 foram recebidos.

Foi feita a chamada da função multiplica e a passagem de parâmetros.

O valor retornado pela função foi armazenado em resultado.

O valor armazenado em resultado foi apresentado.



**10.4 - Protótipo de função em C**

O protótipo de uma função é basicamente, uma declaração da interface da função, ou seja, deve especificar:

* Tipo da função;
* Nome da função;
* Lista de parâmetros que a função necessita;

Exemplo:  
int multiplica\(int N1, int N2\)  
** Programa em C reescrito usando protótipo:**

```c
#include<stdio.h>
#include<conio.h>
/**   Protótipo da função  **/
int multiplica(int N1, int N2);

int main(void)
{
  int V1, V2, resultado;
  printf("Digite o primeiro valor:");
  scanf("%d", &V1);
  printf("Digite o segundo valor:");
  scanf("%d", &V2);

  //chama a função e recebe o retorno
  resultado = multiplica(V1,V2);
  printf("Resultado = %d\n", resultado);
  getch();
  return 0;
}

int multiplica(int N1, int N2) //multiplica recebe N1,N2 e retorna um int
{
  int resultado;
  resultado = N1 * N2;
  return(resultado); //retornando o valor para main
}
```

**10.5 - Função sem retorno**

Em C, é possível criar funções que não retornam nenhum valor.

Normalmente, isto é feito quando queremos executar um bloco de comandos, mas estes comandos não precisam retornar nada.

Neste caso, devemos usar void no tipo de retorno do cabeçalho da função.

Se a função não recebe nenhum parâmetro, também colocamos void no local da listagem dos parâmetros.  
exemplo:

```c
void imprime_cabec(void)
{
  printf("******************************\n");   
  printf("*       LINGUAGEM C          *\n");
  printf("******************************\n");   

  return; /** retorno de uma função void  **/
}
```

Para funções do tipo void, \(ou seja sem retorno\) devemos usar o comando return;

Note bem que este return não contém nenhum parâmetro.

Já que não é preciso retornar nenhum parâmetro e se eu não escrever o comando return?

Se a instrução return for omitida, alguns compiladores vão gerar mensagens de advertência \(warning\), pois o padrão ANSI C recomenda a utilização da instrução.

**Exemplo de programa usando funções com e sem retorno.**

```c
#include<stdio.h>
#include<conio.h>

/******* Área dos protótipos ******/
void imprime_cabec(void);
int multiplica(int N1, int N2);
/******* fim dos protótipos *******/

/* ******* FUNÇÃO PRINCIPAL *******/
int main(void)
{
  int V1=0, V2=0, resultado=0;
  //Chamada da função imprime_cabec
  imprime_cabec();

  printf("Digite o primeiro valor:");
  scanf("%d", &V1);
  printf("Digite o segundo valor:");
  scanf("%d", &V2);

  //chama a função e recebe o retorno
  resultado = multiplica(V1,V2);
  printf("Resultado = %d\n", resultado);

  getch();
  return 0;
}
/* ******** FIM DA FUNÇÃO PRINCIPAL *******/

/* --------- Corpo das funções --------- */
/*
***** Função imprime_cabec *****
Parâmetros de entrada: não tem (void)
Objetivo: imprimir cabeçalho na tela
Tipo de retorno: não tem (void)
*/
void imprime_cabec(void)
{
  printf("******************************\n");
  printf("*       LINGUAGEM C          *\n");
  printf("******************************\n\n");

  return;/* retorno de uma função void  */
}

/****** Função multiplica *****
* Parâmetros de entrada: N1, N2 ambos int
* Objetivo: multiplicar valores
* Tipo de retorno: int (resultado);
**/
//multiplica recebe N1,N2 e retorna um int
int multiplica(int N1, int N2)
{
  int resultado;
  resultado = N1 * N2;

  //retornando o valor para main
  return(resultado);
}
```

Neste programa utilizamos duas funções, uma delas com retorno de valor multiplica\(\) e outra delas sem retorno imprime\_cabec\(\).

Primeiramente, declaramos todos os protótipos das funções antes da main.

Na função main\(\) são feitas as chamadas para as outras funções.

Após a finalização do código da main\(\), são implementados os corpos das outras funções.

Quando a função main\(\) chama \(invoca\) outra função, o programa “salta” para o trecho de código da função que foi chamada, executa esta função e depois retorna novamente para a função principal main\(\).



**10.6 - Referências:**

CASAVELHA, Eduardo. Funções em C. Disponível em: http://linguagemc.com.br/funcoes-em-c . Acessado em novembro de 2017.

