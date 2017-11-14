# Vetores

###### Por Eduardo Gomes - [Github](https://github.com/elgsantos)

O vetor \(também chamado de array\) é um tipo de estrutura de dados **homogênea**, isto é, capaz de armazenar um conjunto de dados do mesmo tipo, possui um tamanho fixo e uma só dimensão, permitindo armazenamento de diversos valores em apenas uma variável.

Em vez de criar diversas variáveis, como: valor1, valor2, …, valor99, podemos declarar somente um vetor com _n_ espaços em memória conforme a seguir:

![](/assets/vetor1.png)

Desta forma poderemos acessar com o mesmo nome de variável, e somente passando a posição de cada elemento, que chamamos de **índice**, é o que define a posição da variável no vetor, da seguinte forma: vetor\[0\], vetor\[1\], ..., vetor\[99\].

Na linguagem C, assim como muitas outras linguagens, **o vetor é indexado a partir da posição zero**. Portanto, o primeiro elemento de um vetor possui a posição de índice 0, e o último elemento se encontrará no último índice do vetor, que é: _o total de elementos no vetor - 1._

## Declarando um vetor em C

**Sintaxe:**

```c
tipo NomeVetor[tamanho];
```

**Exemplo:**

Declaração do vetor do tipo int com 5 números:

```c
int vetor[5];
```

## Inicialização

Podemos inicializar os valores de um vetor diretamente na sua declaração, como no exemplo a seguir:

```c
int vetor[5] = {15, 20, 5, 10, 50};
```

A quantidade de elementos passados dentro das chaves { } não pode ultrapassar o número de elementos que definimos na declaração dentro dos colchetes \[ \].

É possível inicializar também omitindo o número de elementos dentro dos colchetes, dessa forma o número de elementos será inicializado com a quantidade de elementos que passarmos nas chaves, desta forma:

```c
int vetor[] = {15, 20, 5, 10, 50};
```

Criamos exatamente o mesmo vetor que no exemplo anterior.

É possível também atribuir um valor diretamente a uma posição específica do vetor. No exemplo abaixo atribuímos o número **50 **na **quinta** posição do vetor.

```c
vetor[4] = 50;
```

Abaixo podemos ver uma representação deste vetor na memória.

| 15 | 20 | 5 | 10 | 50 |
| :---: | :---: | :---: | :---: | :---: |


## Acessando os elementos de um vetor

Para acessar uma posição específica do vetor devemos utilizar o nome do vetor e o índice que desejamos acessar.

Por exemplo: Desejamos imprimir na tela um valor do vetor.

```c
printf("%d", vetor[0]);
```

No código acima, **vetor\[0\]**, faz referência ao elemento armazenado no vetor, na posição \(índice\) zero.

### Imprimindo todos os valores na tela

Para não precisarmos imprimir os elementos um a um, utilizamos, uma estrutura de repetição.  
No exemplo abaixo utilizamos o _**for**_:

```c
int i; //a variável i representará o índice do vetor
for(i = 0; i < 5; i++) //i vai variar de 0 até 4, ou seja, até o quinto índice do vetor
    printf("%d ", vetor[i]);
```

### Lendo os valores do usuário para o preenchimento do vetor

Conforme o exemplo anterior, podemos utilizar uma estrutura de repetição para ler dados do usuário para dentro do vetor.

```c
for(i = 0; i < 5; i++)
    scanf("%d", &vetor[i]);
```

## Exercícios

1 - Crie um vetor do tipo _**float** _chamado _**notas**_ de 3 posições que possuirá os seguintes valores: _9.0, 10.0 e 8.5_

2 - Mostre os valores do vetor do exercício anterior na tela

3 - Utilize uma estrutura de repetição para ler do usuário as notas. \(_ %f permite receber dados do tipo float _\)

4 - Crie um vetor de _inteiros_ chamado _vet _de 5 posições em que cada elemento possua o valor de seu índice. Por exemplo, no elemento do primeiro índice deverá conter o valor 0 e assim por diante. Utilize uma estrutura de repetição para atribuir os valores.

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

printf("O maior elemento é %d\n",maior); //deverá ser imprimido o valor 4 caso o vetor seja igual ao do exercício 4
```



