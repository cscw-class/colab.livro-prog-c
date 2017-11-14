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

Cada objeto na memória ocupa um endereço, que é o endereço do primeiro byte.

Exemplo de declarações:

```
         char c;

         int i;

         struct {

         int x,y;

         }ponto;.

        int v\[4\];
```

Exemplo de alocação de espaço na memórias das variáveis declaradas:

```
        c            89421

        i             89422

        ponto    89426

       v\[0\]        89434

       v\[1\]        89438

       v\[2\]        89442

       v\[3\]        89446
```

### 14.2 - Operadores

#### 14.2.1 - Operador Unário & \("endereço de"\):

Quando aplicado a variável, resulta no endereço da posição de memória reservada para a mesma.

Nos exemplos dados acima teríamos que &c = 89421, &i = 89422, &v\[2\] = 89442, ...

**Obs: **Não confundir  o uso do **&**  com o operador lógico _**and**_, que se escreve **&&** em C..

#### 14.2.2 - Operador Unário \* \("conteúdo de"\):

Aplicado a variáveis do tipo ponteiro ponteiro, acessa o conteúdo dom endereço de memória armazenado pela variável ponteiro.

Para cada tipo existente há um tipo de ponteiro que pode **armazenar endereços de memória** , onde existem valores do tipo correspondente armazenados.

/\*variável inteiro \*/

**int a;**

/\*variável ponteiro para inteiro \*/

**int \*p;**

### 14.3 - Ponteiros

A utilização de ponteiros em linguagem C é uma das características que tornam a linguagem tão flexível e poderosa. Ponteiros ou apontadores, são variáveis que **armazenam o endereço de memória de outras variáveis**.

Quando um ponteiro \(a variável\) contém um determinado endereço, dizemos que ele aponta para o endereço de memória. Assim, dizemos que um ponteiro “aponta” para uma variável quando contém o endereço da mesma. Ele pode apontar para qualquer tipo de variável.

Para animar um pouco, abaixo um link sobre ponteiros:

[https://www.youtube.com/watch?v=r7f-aR7vgg0](https://www.youtube.com/watch?v=r7f-aR7vgg0)

#### 14.3.1 - Utilização dos Ponteiros

Ponteiros são muito úteis quando uma variável tem que ser acessada em diferentes partes de um programa.

Neste caso, o código pode ter vários ponteiros espalhados por diversas partes do programa, “apontando” para a variável que contém o dado desejado.

Caso este dado seja alterado, não há problema algum, pois todas as partes do programa tem um ponteiro que aponta para o endereço onde reside o dado atualizado.

Existem várias situações onde ponteiros são úteis, por exemplo:

* Alocação dinâmica de memória
* Manipulação de arrays.
* Para retornar mais de um valor em uma função.
* Referência para listas, pilhas, árvores e grafos.

#### 14.3.2 - **Sintaxe de declaração de ponteiro**

Falamos anteriormente sobre os operadores unários, e vamos relembrar agora o **operador \*** para sintaxe da declaração dos ponteiros.

Como vimos, para definir que uma variável é um ponteiro, utilizamos o operador unário \* na frente do nome da variável:

```
    **tipo \*nome\_ponteiro;**
```

Onde temos:

```
   **tipo**: é o tipo de dado da variável cujo endereço o ponteiro armazena.

   **\*nome\_ponteiro**: O nome da variável ponteiro.
```

Exemplo de declaração de ponteiro:

```
   **int \*ptr;**
```

###### ![](/assets/ponteiro1.png)Fonte: Dept. Informática - PUC-Rio

###### 

![](/assets/ponteiro2.png)

###### Fonte: Dept. Informática - PUC-Rio

| ![](/assets/ponteiro3.png) | ![](/assets/p4.png) |
| :--- | :--- |
| Erro na atribuição **\*p=3**, pois utiliza a memória apontada por **p** para armazenar o valor 3, sem que p tivesse sido  iniciali-zada, logo armazena 3 em um espaço  de  memória  desco-nhecido. | Atribuição correta de **\*p = 3**, onde **p** aponta para **c**  e  a  atri-buição armazena 3 no espaço de memória reservado para **c** |

###### Fonte: Dept. Informática - PUC-Rio

### 14.4 - Exercícios

Faça agora os exercícios. Acesse a lista de exercícios deste e-book [clicando aqu](https://www.gitbook.com/book/alexsalgado/introducao-a-programacao-em-c/edit#/edit/master/lista-de-exercicios.md?_k=6dkdni)i.





**Obs:** _Ponteiros é uma conteúdo muito extenso. Que novos alunos venha complementar este trabalho inicial!_

#### 

#### Referências:

_** FEOFILOFF**, Paulo;** Endereços e Ponteiros**. Página eletrônica do ime.usp.br. Disponível em &lt;_[_https://www.ime.usp.br/~pf/algoritmos/aulas/pont.html_](https://www.ime.usp.br/~pf/algoritmos/aulas/pont.html)_&gt;. Acessado em 07 de novembro de 2017._

**DELGADO**,Armando Luiz Nicolini; **Ponteiros**. _Página eletrônica do inf.ufpr.br. Disponível em &lt;_[_http://www.inf.ufpr.br/cursos/ci067/Docs/NotasAula/notas-28\_Ponteiros.html_](http://www.inf.ufpr.br/cursos/ci067/Docs/NotasAula/notas-28_Ponteiros.html)_&gt;. Acessado em 07 de novembro de 2017._

**CASAVELLA**,Eduardo; Intellectuale. Tecnologia e Treinamento. _Página eletrônica_. _Página eletrônica.. Disponível em &lt;_[_http://www.inf.ufpr.br/cursos/ci067/Docs/NotasAula/notas-28\_Ponteiros.html_](http://linguagemc.com.br/ponteiros-em-c/)_&gt;. Acessado em 12 de novembro de 2017._

