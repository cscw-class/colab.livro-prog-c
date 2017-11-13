# Lista de Exercícios, por capítulos.

## Capítulo 14 - Ponteiros

##### Exercício 1: teste seus conhecimentos online.

[http://www.cprogressivo.net/2013/03/Questoes-com-gabarito-sobre-Ponteiros-em-C.html](http://www.cprogressivo.net/2013/03/Questoes-com-gabarito-sobre-Ponteiros-em-C.html)

##### Exercício 2: Quais serão os valores de x, y e p ao final do trecho de código

abaixo?

int x, y, \*p;y = 0;

p = &y;

x = \*p;

x = 4;

\(\*p\)++;

--x;

\(\*p\) += x;

##### Exercício 3: Os programas \(trechos de código\) abaixo possuem erros. Qual\(is\)?

Como deveriam ser?

a\)

void main\(\) {

int x, \*p;

x = 100;

p = x;

printf\(“Valor de p: %d.\n”, \*p\);}

b\)

void troca \(int \*i, int \*j\) {

int \*temp;

\*temp = \*i;

\*i = \*j;

\*j = \*temp;}

c\)

char \*a, \*b;

a = "abacate";

b = "uva”;

if \(a &lt; b\)

printf \("%s vem antes de %s no dicionário", a, b\);

else

printf \("%s vem depois de %s no dicionário", a, b\);

##### Exercício 4: Suponha que os elementos do vetor v são do tipo int e cada int ocupa 8 bytes no seu computador. Se o endereço de v\[0\] é 55000, qual o valor da expressão v + 3?



##### Exercício 5: Suponha que v é um vetor. Descreva a diferença conceitual entre as expressões v\[3\] e v + 3.



##### Exercício 6: Qual o conteúdo do vetor a depois dos seguintes comandos \(sem usar o computador\): int a\[99\];for \(i = 0; i &lt; 99; ++i\) a\[i\] = 98 - i;for \(i = 0; i &lt; 99; ++i\) a\[i\] = a\[a\[i\]\]; 



##### Exercício 7: O que significa o operador asterisco em cada um dos seguintes casos:

a\) int \*p;

b\) cout &lt;&lt; \*p;

c\) \*p = x\*5;

d\) cout &lt;&lt; \*\(p+1\);

