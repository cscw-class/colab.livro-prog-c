# **Capítulo 5.1: Entrada e Saída de Dados:printf\(....\)**

###### autor: Iann Rezende Zukowski 

O **PRINTF** é usado, na linguagem **C** quando se deseja "escrever" algo na tela, ou seja, mostrar alguma mensagem para interagir com o usuário.

Para usar o **PRINTF** precisamos da biblioteca **STDOI.H** e sua estrutura é: printf depois parentes aspas e a mensagem que deseja escrever. Além da mensagem podemos mostrar o valor das variáveis. Para isso é preciso usar o % e o tipo da variável\(int, float, char,etc\), conforme visto no capítulo 3

Exemplo:

1- escrever na tela uma mensagem, o usuário:

**`#include<stdoi.h>`**

**`int main()`**

**`{`**

**`printf("Mensagem para o usuário\n");`**

**`return 0;`**

**`}`**

**2- escrever o valor da variável\(tipo inteiro\)**

**`#include<stdoi.h>`**

**`int main()`**

**`{`**

**`int idade=30;`**

**`printf("A idade do aluno é %d\n",idade);`**

**`return 0;`**

**`}`**

**obs1:** Note que quando mostramos o valor de uma variável, a variável ver, escrita dentro do comando **PRINTF**

**obs2**: em ambos os exemplos foi utilizado** \n** que serve para pular linha.

  


