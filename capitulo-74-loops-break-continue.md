# **Capítulo 7.4: Loops - Break / Continue**

Por Renata Machado



         O comando **BREAK** é geralmente associado às estruturas de repetição \([FOR](https://alexsalgado.gitbooks.io/introducao-a-programacao-em-c/content/capitulo-71-for.html), WHILE, DO WHILE\) e ao comando SWITCH e é utilizado para realizar uma parada imediata do bloco de comando em execução no momento de sua chamada.

         Em estruturas de repetição sua função é evitar que o programa continue rodando o laço após ter encontrando a informação que necessitava. Ex:



`void busca ( Int v)`

`{`

`      int b;`

`      For (b=0; b<100; b++) {`

`           Printf (“ o numero eh: %d”, b);`

`           If (b==v) break; // se b for igual o valor buscado, o programa sairá do FOR e continuará com sua execução`

`      }`

`}`





	Já no comando SWITCH, sua função é evitar que o programa continue fazendo as verificações caso já tem encontrando a informação:



`#include <stdio.h>`

`#include <conio.h>`

``

`int main (void)`

`{`

`     intvalor;`

`     printf("Digite um valor de 1 a 7: ");`

`      scanf("%d", &valor);`

`     switch( valor )`

`   {`

`         case1 :`

`                 printf("Domingo\n");`

`          break;`

`         case2 :`

`                 printf("Segunda\n");`

`         break;`

`         case3 :`

`                 printf("Terça\n");`

`         break;`

`         case4 :`

`                 printf("Quarta\n");`

`         break;`

`        case5 :`

`                printf("Quinta\n");`

`        break;`

`        case6 :`

`               printf("Sexta\n");`

`        break;`

`        case7 :`

`               printf("Sabado\n");`

`        break;`

``

`      default:`

`              printf("Valor invalido!\n");`

`         }`

`getch();`

`return0;`

`}`





Assumindo que o valor informado seja 5, o programa rodará até o **case 5**, imprimirá “Quinta” e será encerrado.



