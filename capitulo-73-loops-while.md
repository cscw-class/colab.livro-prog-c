# **Capítulo 7.3: Loops - while**



**7.3.1 – Descrição:**

O while, "enquanto" em inglês, é um laço que ordena o computador a executar determinados comandos enquanto uma condição for verdadeira. Isso faz com que um comando seja executado uma vez a cada verificação da condição. Esses comandos podem ser apenas uma instrução do C ou um bloco de instruções entre chaves.

De modo geral o comando sempre deve ser elaborado de forma que se leve a condição de execução a ser falsa em algum momento, de forma a interromper o laço para que o resto do programa entre em execução.



**7.3.2 – Pseudocódigo:**

A estrutura Enquanto … Faça equivale a estrutura while em linguagem C.



**7.3.3 – Sintaxe:**

```
Iniciar a variável de controle

Enquanto (condição) faça
Início
    Instruções;
    Atualizar a variável de controle;
Fim;
```

* Lembrando que chamamos de variável de controle a variável testada na condição.
* Para que seja possível fazer o teste, a variável de controle deve ter sido inicializada previamente.
* Observe que o teste da condição ocorre no início do laço.

* Enquanto a condição permanecer verdadeira, são executadas as instruções.

* Quando a condição se tornar falsa, o processamento será desviado para fora do laço.



**Atenção: **Note bem, que caso a condição seja falsa logo no início, as instruções do laço são ignoradas.



**7.3.4 – Utilizando em C:**

```
while (condição)
comando;
```

* Onde 'condição' é a condição de execução do laço while.



**Exemplo 1:**

O código abaixo mostra o uso do laço while para imprimir na tela do número 1 ao número 10. Perceba o uso de uma variável inteira intituladacontador. Esta variável é utilizada para armazenar um valor a ser impresso bem como participar da condição de execução do laço. Assim que a variável atingir o valor 11 o programa segue para o comando logo após o laço.

```
#include <iostream>

using namespace std;

int main()
{
  int contador;               // Declara a variável contador.
  contador=1;                 // contador recebe o valor 1.
  while (contador<=10)        // Enquanto contador for menor ou igual a 10.
  {
    cout << contador << endl; // Imprime contador.
    contador++;               // Incrementa contador em uma unidade.
  }
  return 0;
}
```



**Exemplo 2:**



```
#include <stdio.h>
#include <conio.h>
int main(void)
{
    int contador = 1;      //declarando e inicializando a variável de controle
    while (contador <= 10)       // Testando a condição
    {
          printf("%d ", contador); //Executando um comando dentro do laço 
          contador++; //atualizando a variável de controle
    }
     
    getch(); 
    return 0; 
}
```



**Visualização da tela de execução do programa:**

![](/assets/img_cap7_3.jpg)

Inicialmente, a variável de controle denominada contador foi declarada e inicializada com o valor 1. O teste da condição while é realizado , e como o contador é menor que 10, então a condição é verdadeira.

Como a condição é verdadeira, o programa entra dentro do corpo do laço e executa o printf, exibindo o valor da variável contador. Após executar o comando printf, o contador é incrementado.

Depois do incremento, a condição é testada novamente e enquanto for verdadeira, os comandos são executados de novo, até que a condição se torne falsa. A condição falsa faz com que o laço seja encerrado.







**7.3.5 - Referências:**

\[1\] Programar em C++/Estruturas de repetição, 2017. Disponível em:[https://pt.wikibooks.org/wiki/Programar\_em\_C%2B%2B/Estruturas\_de\_repeti%C3%A7%C3%A3o](https://pt.wikibooks.org/wiki/Programar_em_C%2B%2B/Estruturas_de_repetição). Acesso em Novembro de 2017

\[2\] CASAVELHA, Eduardo. O comando while em C. Disponível em:[http://linguagemc.com.br/o-comando-while-em-c/](http://linguagemc.com.br/o-comando-while-em-c/). Acesso em Novembro de 2017

