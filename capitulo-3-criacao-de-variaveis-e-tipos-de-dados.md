# Capítulo 3

## Criação de variáveis e tipos de dados

###### Autor: [Felipe Prado](https://github.com/fpterrific)

---

###Introdução
Para que sua aplicação em C se torne bem útil, lança-se mão do uso de variáveis. Mas afinal, o que seriam elas?

```c
int numero
char letra
```

Variáveis são partes reservadas na memória do programa que são utilizadas para guardar informações. Elas pode servir, tanto para cálculos,

```c
int numero1;
```

como para guardar textos e outros tipos de informação.

```c
char letra;
```

###Declaração de variáveis
Em C, as variáveis devem ser declaradas antes de serem utilizadas. Acima, foram utilizados exemplos de variáveis que começam com letras. Nesta linguagem, as variaveis devem iniciar com letra minuscula ou um caractere underscore (_):

```c
int num;
char caractere;
float _produto;
```

Uma variável não pode iniciar com números. Expressões reservadas do sistema  ( ``if, else, while, ... `` ) também não podem ser utilizadas para nomear as váriáveis.
Exemplo incorreto:

```c
int 1;
```

Podemos atribuir valores às variáveis, para isto, basta colocar um sinal de igual (=) após o nome da variável:

```c
int num;
num = 1;
```

Apesar de não podermos iniciar os nomes das variáveis com letras maiúsculas ou números, eles podem aparecer nos demais caracteres da variável. Lembre-se que, por ser _case sensitive_, as variáveis deverão ser cahamdas do mesmo modo em que foram declaradas. Caso contrário, seu programa acusará um erro:

```c
int nUm;
num = 1; //aqui seu programa acusará um erro
```

###Tipos de dados
Em C, existem cinco tipos, chamados primitivos, de dados:
``char, int, float, double e void``

Com exceção do void (que é mais utilizado para desenvolver funções que nada retornam ou que nada recebem, como será visto mais a frente), todos os outros tipos são capazes de guardar informações.

O tipo char é utilizado para guardar um caractere