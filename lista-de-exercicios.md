# Lista de Exercícios, por capítulos.

## Capítulo 2 - Olá Mundo

2.1- Faça um programa em C que imprima a mensagem "Segundo Programa"

2.2- Faça um programa em C que imprima a mensagem "Segundo programa" duas vezes.

## Capítulo 3 - Criação de variáveis e tipos de dados

3.1 - Dos exemplos abaixo, quais estão corretos em relação a declaração de variáveis:

* int 123
* char caractere
* double Um

3.2 - Como atribuir valores às variáveis?

3.3 - Quais são os cinco tipos primitivos de dados em C?

3.4 - É possível utilizar qualquer nome para denominar uma variável? Por que?

## Capítulo 6.2 - Tomadas de Decisões \(Switch\)

#### Exercício

1- Utilizando a ferramenta switch case, crie um programa que diga receba do usuario um numero de 1 a 12 e o programa deve retornar ao usuario qual nome do mes. Exemplo: 1 = Janeiro, 2 = Fevereiro;

2 - Construa em  C uma mini calculadora utilizando Switch Case, onde o usuário deve selecionar se deseja fazer Soma, Subtração, Multiplicação ou Divisão e pedir ao usuário para inserir dois valores.

## Capítulo 8: Vetores

1 - Crie um vetor do tipo **float **chamado **notas** de 3 posições que possuirá os seguintes valores: \_9.0, 10.0 e 8.5

2 - Mostre os valores do vetor do exercício anterior na tela

3 - Utilize uma estrutura de repetição para ler do usuário as notas. \(_ %f permite receber dados do tipo float _\)

4 - Crie um vetor de _inteiros_ chamado vet de 5 posições em que cada elemento possua o valor de seu índice. Por exemplo, no elemento do primeiro índice deverá conter o valor 0 e assim por diante. Utilize uma estrutura de repetição para atribuir os valores.

5 - **Desafio:** Crie um loop que compare cada valor do vetor para encontrar o maior. Utilize uma variável para armazenar o maior valor do vetor, e no final imprima o maior valor. Pode ser utilizado o vetor do exercício anterior.

## Respostas

Questão 1:

```c
float notas[3] = {9.0, 10.0, 8.5};
```

Questão 2:

```c
int i;
for(i = 0; i < 3; i++)
    printf("%.1f ", notas[i]); //%.1f exibe o valor do tipo float com uma casa decimal. Ex: 9.5
```

Questão 3:

```c
for(i = 0; i < 3; i++)
    scanf("%f", &notas[i]);
```

Questão 4:

```c
int vet[5];
for(i = 0; i < 5; i++)
    vet[i] = i; //o valor do elemento será o mesmo valor do índice
```

Questão 5:

```c
int maior = vet[0];  // assume que o primeiro é o maior

for(i=0; i<5; i++)
    if (vet[i] > maior)
        maior = vet[i];

printf("O maior elemento é %d\n",maior); // o \n foi utilizado apenas para pular linha
/*deverá ser imprimido o valor 4 caso o vetor seja igual ao do exercício 4*/
```

## Capítulo 9 - Matrizes

1 - Faça um programa que lê uma matriz de 3 x 3 elementos usando um comando "for" e  multiplica cada elemento por 5 e imprime o resultado.

2 - Escrever um algoritmo para ler uma matriz 7 x 4 contendo valores inteiros. Após, encontrar o menor valor contido na matriz e sua posição.

#### Respostas

1-

![](/assets/exerMatriz1.png)

2-

![](/assets/exerMatriz2.png)

## Capítulo 9.1- Matrizes Dinâmicas

Faca um programa que multiplique duas matrizes. O programa devera' estar  estruturado de maneira que:  
 1- o usuario forneca as dimensoes das matrizes \(teste se as dimensoes sao compativeis,  isto e', se as matrizes podem ser multiplicadas\);  
 2- as matrizes sejam alocadas dinamicamente \(voce pode usar a funcao vista nesta pagina para  isto\);  
 3- as matrizes sejam lidas pelo teclado \(faca uma funcao para leitura das matrizes\);  
 4- as matrizes sejam, entao, multiplicadas \(faca uma funcao para a multiplicacao\);  
 5- a matriz resultante seja apresentada em tela \(faca uma funcao para apresentar a matriz na tela\).

OBS:  
 a\) Faca, tambem, alocacao dinamica da matriz resultante.  
 b\) Caso alguém não conheça o procedimento para a multiplicação de matrizes, segue aqui alguma orientação. Suponha as matrizes A\(mXn\)

```
\| a11  a12 ... a1n \|
```

A = \| a21  a22 ... a2n \|  
    \|  :               \|  
    \| am1  am2 ... amn \|

e B\(nXt\)

```
\| b11  b12 ... b1t \|
```

B = \| b21  b22 ... b2t \|  
    \|  :               \|  
    \| bn1  bn2 ... bnt \|

O elemento ij da matriz C é resultante da multiplicação da linha i de A pela coluna j de B. Portanto, a matriz C \(mXt\) = A\*B será da seguinte forma:

C =  
\| a11\*b11 +a12\*b21 + ... +a1n\*bn1   a11\*b12 +a12\*b22 + ... + a1n\*bn2  ...   a11+b1t +a12\*b2t + ... + a1n\*bnt \|  
\| a21\*b11 +a22\*b21 + ... +a2n\*bn1   a21\*b12 +a22\*b22 + ... + a2n\*bn2  ...   a21+b1t +a22\*b2t + ... + a2n\*bnt \|  
\|                                   ...                                                   ...                   ...                                    ...                                    \|  
\| am1\*b11 +am2\*b21 +...+amn\*bn1   am1\*b12 +am2\*b22 +...+ amn\*bn2  ...   am1+b1t +am2\*b2t +...+amn\*bnt \|

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

## Capítulo 11 - Strcmp e Strcpy

11.1  Construa um programa em C que leia quatro nomes fornecidas pelo usuário através da  entrada padrão e os salve, garantindo que  somente os nomes que não são repetidos serão salvos.

11.2  Seja o código abaixo que recebe uma string e devolve uma cópia da string com as letras minúsculas transformadas em maiúsculas.

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

## 



