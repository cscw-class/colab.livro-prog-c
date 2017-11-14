# Capítulo 3

## Criação de variáveis e tipos de dados

###### Autor: [Felipe Prado](https://github.com/fpterrific)

---

###Introdução
Para que sua aplicação em C se torne bem útil, lança-se mão do uso de variáveis. Mas afinal, o que seriam elas?

```c
int numero
char letra
```

Variáveis são partes reservadas na memória do programa que são utilizadas para guardar informações. Elas pode servir, tanto para cálculos,

```c
int numero1;
int nuemro2;
int recebesoma;
recebesoma = numero1 + numero2;
```

como para guardar textos e outros tipos de informação.

```c
char letra;
letra = "C";
```

###Declaração de variáveis
Em C, as variáveis devem ser declaradas antes de serem utilizadas. Acima, foram utilizados exemplos de variáveis que começam com letras. Nesta linguagem, as variaveis devem iniciar com letra minuscula ou um caractere underscore (_)

```c
int num;
char caractere;
float _produto;
```

Uma variável não pode iniciar com números. Expressões reservadas do sistema  ( ``if, else, while, ... `` ) também não podem ser utilizadas para nomear as váriáveis.
Exemplo incorreto:

```c
int 1;

```

