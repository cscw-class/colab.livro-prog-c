# **Capítulo 13: Typedef**

**Aluna: Eyre Brasil Montevecchi – **[**Github**](https://github.com/eyrebrasil)

#### **13.1. Definição**

A palavra reservada **typedef** é utilizada para criar um alias ou “apelido” para tipos de dados na linguagem C e C++. Desta forma, tipos de dados podem ser organizados segundo a sua função, estruturas \(struct\) podem ter sua utilização simplificada e tipos com declarações de variáveis complexas e longas podem ter sua nomenclatura reduzida e usabilidade melhorada. Sua forma geral é:

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

No trecho de código acima, o nome vetorIntTamMAX é definido como um alias ou uma outra forma mais resumida de declarar um vetor de inteiros com tamanho igual ao valor definido para a constante MAX. Agora, no programa acima, quando quisermos declarar um vetor desse tipo, basta escrever:

```c
vetorIntTamMAX v1;
```

O mesmo se aplica aos demais apelidos criados: para declarar os contadores inteiros do programa acima, podemos utilizar o alias contador, que representa as variáveis do tipo int:

```c
contador i, j;
```

#### **13.2 Indicando o significado em declarações de variáveis**

O typedef pode ser utilizado para dar significados a variáveis, organizando o programa e indicando que essas não são compatíveis dentro do contexto do programa, embora sejam compatíveis para o compilador. Veja o exemplo abaixo, com uma declaração sem a utilização do typedef:

```c
int velocidade_atual ;
int maior_pontuacao;

void congratular(int sua_pontuacao) {
    if (sua_pontuacao > maior_pontuacao)
    ...
    }
}
```

Agora o veja a modificação abaixo, expressando o contexto específicos dos tipos declarados:

```c
typedef int km_por_hora ;
typedef int pontos ;

km_por_hora velocidade_atual ;  
pontos maior_pontuacao ;       

void congratular (pontos sua_pontuacao) {
    if (sua_pontuacao > maior_pontuacao){
    ...
    }
}
```

Os dois trechos de código executam da mesma maneira, mas no segundo trecho, é mais clara a incompatibilidade entre as variáveis velocidade\_atuale maior\_pontuacao, embora sejam ambas do tipo int e comparáveis para o compilador, que não apontaria nenhum problema ao compilar o código abaixo, que está incorreto contextualmente e retornará resultados indesejados para o programa em questão:

```c
velocidade_atual = 100;
maior_pontuacao = velocidade_atual;
```

Porém, o compilador não aceitará modificações através de prefixos para esses apelidos criados. O código abaixo por exemplo, geraria erro de compilação:

```c
typedef int pontos;
unsigned pontos a;
```

**13.3 Utilização com Struct**

**Exercícios**

**Referências**

\[1\] Typedef. Wikipédia, 2017. Disponível em: &lt;[https://en.wikipedia.org/wiki/Typedef](https://en.wikipedia.org/wiki/Typedef)&gt;. Acesso em: 10 nov. 2017.

\[2\] ARAÚJO, Aldrovando Luís Azeredo. Curso de C da UFMG – Aula 11 – Tipos de dados definidos pelo Usuário: o comando typedef. CPDEE/UFMG, 1999. Disponível em: &lt;[http://mtm.ufsc.br/~azeredo/cursoC/aulas/cb60.html](http://mtm.ufsc.br/~azeredo/cursoC/aulas/cb60.html)&gt;. Acesso em: 10 nov. 2017.

