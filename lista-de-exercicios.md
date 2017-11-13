# Lista de Exercícios, por capítulos.

## Capítulo 13 - Typedef

13.1 Considerando a definição abaixo, como seria a declaração das variáveis p1 do tipo int\* e p2 do tipo int\*\*?

```c
typedef int *pontInt;
```

13.2. Simplifique as definições e declarações das _structs_ abaixo, utilizando o _typedef_:

```c
struct ponto{
    int x;
    int y;
};
struct linha{
    struct ponto p1;
    struct ponto p2;
    int distancia;
};

struct linha l1;
```

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

## Capítulo 10 - Funções

1. Crie uma função que receba um valor e informe se ele é positivo ou não.

2. Crie uma função que receba um valor e diga se é nulo ou não.

3. Crie uma função que receba três valores, 'a', 'b' e 'c', que são os coeficientes de uma equação do segundo grau e retorne o valor do delta, que é dado por 'b² - 4ac'

4. Usando as 3 funções acima, crie um aplicativo que calcula as raízes de uma equação do 2o grau:

ax² + bx + c=0

Para ela existir, o coeficiente 'a' deve ser diferente de zero.

Caso o delta seja maior ou igual a zero, as raízes serão reais. Caso o delta seja negativo, as reais serão complexas e da forma: x + iy

1. Crie uma função em linguagem C que receba 2 números e retorne o maior valor.

2. Crie uma função em linguagem C que receba 2 números e retorne o menor valor

3. Crie uma função em linguagem C que receba 3 números e retorne o maior valor, use a função da questão 4.

4. Crie uma função em linguagem C que receba 3 números e retorne o menor valor, use a função da questão 5.

5. Crie uma função em linguagem C chamado Dado\(\) que retorna, através de sorteio, um número de 1 até 6.

6. Use a função da questão passado e lance o dado 1 milhão de vezes. Conte quantas vezes cada número saiu.

A probabilidade deu certo? Ou seja, a porcentagem dos números foi parecida?

1. Crie um aplicativo de conversão entre as temperaturas Celsius e Farenheit.

Primeiro o usuário deve escolher se vai entrar com a temperatura em Célsius ou Farenheit, depois a conversão escolhida é realizada através de um comando SWITCH.

Se C é a temperatura em Célsius e F em farenheit, as fórmulas de conversão são:

C= 5.\(F-32\)/9

F= \(9.C/5\) + 32

1. Um professor, muito legal, fez 3 provas durante um semestre mas só vai levar em conta as duas notas mais altas para calcular a média.

Faça uma aplicação em C que peça o valor das 3 notas, mostre como seria a média com essas 3 provas, a média com as 2 notas mais altas, bem como sua nota mais alta e sua nota mais baixa.

Desafio 1: Programe um aplicativo em C que acha todos os números primos até 1000

Número primo é aquele que é divisível somente por 1 e por ele mesmo.

Desafio 2: Programe um aplicativo em C que recebe dois inteiros e retorna o MDC, máximo divisor comum.

Desafio 3: Programe um aplicativo em C que ache todos os números perfeitos até 1000.

Número perfeito é aquele que é a soma de seus fatores. Por exemplo, 6 é divisível por 1, 2 e 3 ao passo que 6 = 1 + 2 + 3.

Desafio 4: Crie um programa em C que receba um número e imprima ele na ordem inversa.

Ou seja, se recebeu o inteiro 123, deve imprimir o inteiro 321.

