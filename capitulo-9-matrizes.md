# Matrizes

A partir do que foi visto no capítulo anterior, as matrizes são como vetores, porém multidimensionais. A forma mais comum de matrizes multidimensionais são as bidimensionais, que na linguagem C vemos da seguinte forma no momento de sua declaração:

int m\[x\]\[y\];

Abaixo encontramos um exemplo de uma matriz com duas dimensões m\[3\]\[4\]:

![](/assets/import.png)

#### Entendendo as Matrizes

Como vimos acima, as matrizes bidimensionais são definidas com dois eixos \( x e y \) onde a partir da matriz m\[3\]\[4\], pode-se obeservar que:

* O valor \[3\] representa a quantidade de linhas
* O valor \[4\] representa a quantidade de colunas

Esse matriz pode ser definida com o tipo 3 x 4.

Como temos 3 linhas e 4 colunas, podemos realizar um cálculo simples multiplicando 'x' e 'y' e identificar que o total de itens que a matriz apresentada armazena é de 12 itens.

Com isso, uma vez que a matriz é bidimensional, teremos que acessar as posições desta matriz através de dois índices.

Obs.: Como nos vetores, as matrizes possuem índices que permitem que as posições da matriz sejam acessadas.



####  Atibuindo valores a uma Matriz

Para atribuir valores a uma matriz devemos buscar cada posição e a partir disso, preencher a mesma.

Um exemplo pode ser visto abaixo:

//Declaração da Matriz

float m\[4\]\[2\];

//Atribuindo o valor 2 para a primeira posição da matriz, onde esta é encontrada a partir da primeira linha e da primeira coluna.

m\[0\]\[0\] = 2

//Atribuindo o valor 5 para a segunda linha da primeira coluna.

m\[1\]\[0\] = 5



#### Preenchendo Matrizes

Existem diversos métodos para o preenchimento de uma matriz, mas para isso, devemos buscar cada posição e preencher todas através dos índices que nos auxiliam.

Abaixo temos um método de preenchimento de matrizes em que é usado duas estruturas de repetição "for" e duas variáveis do tipo "int" tanto para linha quanto para coluna.

Exemplo

































