# **Capítulo 13: Typedef**

**Aluna: Eyre Brasil Montevecchi – **[**Github**](https://github.com/eyrebrasil)

#### **13.1. Definição**

A palavra reservada **typedef** é utilizada para criar um alias ou “apelido” para tipos de dados na linguagem C e C++. Desta forma, tipos de dados podem ser organizados segundo a sua função e tipos com definições ou declarações de variáveis complexas e longas podem ter sua nomenclatura simplificada. Sua forma geral é:

`typedef antigo_nome novo_nome;`

Abaixo temos exemplos de sua utilização em programas C:

```c
#define MAX 10

int main () {

    typedef int vetorIntTamMAX[MAX];
    typedef char novoChar;
    typedef int contador;
    typedef int *ponteiroInt;

    vetorIntTamMAX v1;
    novoChar c1;
    contador i, j;
    ponteiroInt p1;

  return 0;
}
```

No trecho de código acima, o nome vetorIntTamMAX é definido como um _alias_ ou uma outra forma mais resumida de declarar um vetor de inteiros com tamanho igual ao valor definido para a constante MAX. Agora, no programa acima, quando quisermos declarar um vetor desse tipo, basta escrever:

```c
vetorIntTamMAX v1;
```

O mesmo se aplica aos demais apelidos criados: para declarar os contadores inteiros do programa acima, podemos utilizar o alias contador, que representa as variáveis do tipo _int_:

```c
contador i, j;
```

#### **13.2 Indicando o significado em declarações de variáveis**

O typedef pode ser utilizado para dar significados a variáveis, organizando o programa e indicando que essas não são compatíveis dentro do contexto do programa, embora sejam compatíveis para o compilador. Veja o exemplo abaixo, com uma declaração sem a utilização do _typedef_:

```c
int velocidade_atual;
int maior_pontuacao;

void congratular(int sua_pontuacao) {
    if (sua_pontuacao > maior_pontuacao)
    ...
    }
}
```

Agora o veja a modificação abaixo, expressando o contexto específicos dos tipos declarados:

```c
typedef int km_por_hora;
typedef int pontos;

km_por_hora velocidade_atual;  
pontos maior_pontuacao;       

void congratular (pontos sua_pontuacao) {
    if (sua_pontuacao > maior_pontuacao){
    ...
    }
}
```

Os dois trechos de código executam da mesma maneira, mas no segundo trecho, é mais clara a incompatibilidade entre as variáveis velocidade\_atual e maior\_pontuacao, embora sejam ambas do tipo _int_ e comparáveis para o compilador, que não apontaria nenhum problema ao compilar o código abaixo, que está incorreto contextualmente e retornará resultados indesejados para o programa em questão:

```c
velocidade_atual = 100;
maior_pontuacao = velocidade_atual;
```

Porém, o compilador não aceitará modificações através de prefixos para esses apelidos criados. O código abaixo por exemplo, geraria erro de compilação:

```
typedef int pontos;
unsigned pontos a;
```

#### **13.3 Simplificando definições e declarações**

Podemos também simplificar o nome de tipos mais complexos, como as estruturas de dados \(_struct_\). Veja o trecho de código abaixo:

```c
struct minhaStruct {
    int dado1;
    char dado2;
};
```

Agora que a _struct_ minhaStruct foi definida, para declarar variáveis desse tipo em C, a palavra chave _struct_ é obrigatória:

```c
struct minhaStruct a;
```

Podemos eliminar a utilização da palavra _struct_ de duas formas. Acrescentando a palavra _typedef _à declaração como abaixo:

```c
typedef minhaStruct minhaStructNova;
//declaração agora fica:
minhaStructNova a;
```

Ou combinando a definição e declaração de uma vez só:

```c
typedef struct nomeDaMinhaStruct{
    int dado1;
    char dado2;
} ApelidoDaMinhaStruct;

ApelidoDaMinhaStruct a;
```

Suponha porém, que estamos criando uma estrutura chamada **nodo**. Esta estrutura terá um valor chave e ponteiros que pontam para uma estrutura nodo também. Teríamos que utilizar a seguinte declaração abaixo:

```c
typedef struct nodo{
    int chave;
    struct nodo *prox;
    struct nodo *ante;
} Nodo;
```

Note que precisamos usar a palavra _struct_ para declarar ponteiros para struct nodo, pois o apelido só é definido após o corpo da struct nodo. Para usarmos os ponteiros de forma mais simplificada, basta fazer como o exemplo abaixo:

```c
typedef struct nodo Nodo;
struct Nodo{
    int chave;
    Nodo *prox;
    Nodo *ante;
};
```

#### 1**3.4 Referências**

\[1\] Typedef. Wikipédia, 2017. Disponível em: &lt;[https://en.wikipedia.org/wiki/Typedef](https://en.wikipedia.org/wiki/Typedef)&gt;. Acesso em: 10 nov. 2017.

\[2\] ARAÚJO, Aldrovando Luís Azeredo. Curso de C da UFMG – Aula 11 – Tipos de dados definidos pelo Usuário: o comando typedef. CPDEE/UFMG, 1999. Disponível em: &lt;[http://mtm.ufsc.br/~azeredo/cursoC/aulas/cb60.html](http://mtm.ufsc.br/~azeredo/cursoC/aulas/cb60.html)&gt;. Acesso em: 10 nov. 2017.

