# Capítulo 2

## Primeiro programa em C, Olá Mundo!

###### autor: Yuri Lima

Quando aprendemos uma nova linguagem de programação tradicionalmente criamos um programa "Olá Mundo"/"Hello World". Que é simplesmente mostrar na tela uma frase, no caso "Olá Mundo".

No aconselho que seja utilizado a IDE\(Integrated development environment/Ambiente de Desenvolvimento Integrado\) Dev C++ pela simplicidade e praticidade da mesma.

Basta seguir os passos abaixo: 

**Exemplo:**

**1- Abrir IDE:**

**2- Colar código:**

`#include<stdio.h>`

`int main()`

`{`

`printf("Olá Mundo \n");`

`system("pause");`

`return 0;`

`}`

**Obs:**

|  |  |
| :--- | :--- |
| \#include&lt;stdio.h&gt; | Incluindo a biblioteca stdio.h, arquivos com extensão .h costumam ser bibliotecas em C. |
| int main\(\){ | Abertura da função principal, conhecida como main\(\), int no começo quer dizer que o mesmo retornará um inteiro. |
| printf\("Conteúdo"\) | O comando printf\("Conteúdo"\) é para mostrar na tela o conteúdo que está entre "". |
| system\("pause"\) | Por default programas em C fecham automaticamente no final, o comando system\("pause"\) é para congelar a tela após mostrar a mensagem para que assim o usuário consiga visualizar. |
| return 0 | É um comando default dos programas em c, informa um retorno da função main, pode ser 0 ou qualquer numero inteiro, porque foi indicado no começo que a mesma retornaria um numero int.  |

**3- Salvar com extensão .c**

![](/assets/extensaoc.png)

**4- Compilar e Rodar:**

![](/assets/compile/run.png)



**Exercícios:**

1- Faça um programa em C que imprima a mensagem "Segundo Programa"

2- Faça um programa em C que imprima a mensagem "Segundo programa" duas vezes.

