# **Capítulo 5.1: Entrada e Saída de Dados:printf\(....\)**

###### autor: Iann Rezende Zukowski

O comando printf é usado, na linguagem c quando se deseja "escrever" algo na tela, ou seja, mostrar alguma mensagem para interagir com o usuário.

Para usar o printf precisamos da biblioteca stdio.h e sua estrutura é: printf depois parentes aspas e a mensagem que deseja escrever. Além da mensagem podemos mostrar o valor das variáveis. Para isso é preciso usar o % e o tipo da variável\(int, float, char,etc\). Abaixo, temos uma tabela com os tipos de variáveis:

| Tipo |  |
| :--- | :--- |
| char | %c |
| int | %d |
| float | %f |

**Exemplo:**

**1- escrever na tela uma mensagem, o usuário:**

`#include<stdio.h>`

`int main()`

`{`

`printf("Mensagem para o usuário\n");`

`return 0;`

`}`

**2- escrever o valor da variável\(tipo inteiro\)**

`#include<stdio.h>`

`int main()`

`{`

`int idade=30;`

`printf("A idade do aluno é %d\n",idade);`

`return 0;`

`}`

**obs1:** Note que quando mostramos o valor de uma variável, a variável deve ser, escrita dentro do comando printf

**obs2**: em ambos os exemplos foi utilizado** \n** que serve para pular linha.

**Obs3: **para imprimir uma string, precisamos de uma estrutura de repetição que será abordada nos próximos capítulos

**Exercícios:**

1- Faça um programa em C que imprima a mensagem "estou programando em c"

2- Faca um programa em C que imprima o valor de uma variável do tipo float

