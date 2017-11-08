# 14 - Ponteiros

_**Por Gilberto Roque Sonoda**_

Ponteiros são fundamentais em qualquer linguagem de programação.A linguagem C permite o armazenamento e a manipulação de valores de endereços na memória e** isto é feito através dos ponteiros**. Todo aluno de programação tem que dominar o conhecimento de ponteiros; apesar de um pouco complicado no início, com o estudo, e com muita prática, você conseguirá aprender.

### 14.1- Endereço de Memória

Para início de conversa vamos valar sobre os endereços de memória RAM, que é uma sequência de bytes, e cada um deles armazena um de 256 valores possíveis. Os bytes são numerados sequencialmente e o número de cada byte é o seu endereço.

Os objetos na memória ocupam uma quantidade de específica de  bytes consecutivos. Abaixo um tabela com a quantidade de bytes ocupada por cada objeto:

| Objeto | Quantidade de bytes |
| :---: | :---: |
| Bool | 1\(apesar de usar apena 1 bit\) |
| Char | 1 |
| Int | 4 |
| Long Int | 8 |
| Double | 8 |

Cada objeto na memória ocupa um endereço, que é o endereço do primeiro byte. Por exemplo

char c;

int i;

struct {int x,y;}ponto;

int v\[4\];

c            89421

i             89422

ponto    89426

v\[0\]        89434

v\[1\]        89438

v\[2\]        89442

v\[3\]        89446



### 14.2 - Operadores

#### 14.2.1 Operador Unário & \("endereço de"\):

Quando aplicado a variável, resulta no endereço da posição de memória reservada para a mesma.

#### 14.2.2 Operador Unário \* \("conteúdo de"\):

Aplicado a variáveis do tipo ponteiro ponteiro, acessa o conteúdo dom endereço de memória armazenado pela variável ponteiro.



Para cada tipo existente há um tipo de ponteiro que pode **armazenar endereços de memória** , onde existem valores do tipo correspondente armazenados.

/\*variável inteiro \*/

**int a;**

/\*variável ponteiro para inteiro \*/

**int \*p;**

# em construção

#### Referências:

_** FEOFILOFF**, Paulo; Endereços e Ponteiros. Página eletrônica do ime.usp.br. Disponível em &lt;_[_https://www.ime.usp.br/~pf/algoritmos/aulas/pont.html_](https://www.ime.usp.br/~pf/algoritmos/aulas/pont.html)_&gt;. Acessado em 07 de novembro de 2017._

**DELGADO**,Armando Luiz Nicolini; Ponteiros. _Página eletrônica do inf.ufpr.br. Disponível em &lt;_[_http://www.inf.ufpr.br/cursos/ci067/Docs/NotasAula/notas-28\_Ponteiros.html_](http://www.inf.ufpr.br/cursos/ci067/Docs/NotasAula/notas-28_Ponteiros.html)_&gt;. Acessado em 07 de novembro de 2017._

