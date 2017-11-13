# Capítulo 6.2: Tomada de Decisões - If

##### **Autor: **[**Pedro Teixeira Bisognin**](https://github.com/Pedroteixeirabisognin)

#### Introdução

Muitos comandos em C contam com um teste condicional que determina o curso da ação. Uma expressão condicional chega a um valor verdadeiro ou falso. Em C, ao contrário de muitas outras linguagens, um valor verdadeiro é qualquer valor diferente de zero, incluindo números negativos. Um valor falso é 0. Esse método para verdadeiro e falso permite que uma ampla gama de rotinas sejam codificadas de forma extremamente eficiente, como você verá em breve.

#### COMANDOS DE SELEÇÃO

C suporta dois tipos de comandos de seleção: **if **e **switch**. Além disso o operador "**?**"\\(também conhecido como if ternário\\) é uma alternativa ao if em certas circunstâncias. Onde o comando pode ser único, um bloco de comandos ou nada\\( no caso de comandos vazios\\). A clasula else é opcional.

Expressão um único comando:

```
//A forma geral da sentença if é:
if(expressão) comando;
else comando;
```

Expressão de mais de um comando:

```
if(expressão){
 comando1;
 comando2;
     .
     .
     .
}else{
 comando1;
 comando2;
     .
     .
     .
}
```

Expressão para if ternário:

`Condição ? verdadeiro : falso`

Se a expressão é verdadeira \\(algo diferente de 0\\), o comando ou bloco que forma o corpo do if é executado; caso contrário, o comando ou bloco que o corpo do else \\(se existir\\) é executado. Lembre-se de que apenas o código associado ao if ou o código associado ao else será executado, nunca ambos.

**O Else if**

Também existe o operador Else if, que nada mais é do que um if que deu false e foi para outro if, exemplo:

Expressão Else if:

```
if(expressão){

   comando;

}else if{

   comando_do_segundo_if;

}else{

   comando_do_segundo_if;
}
```

**Exercícios**

1\) Crie um programa ao qual imprima na tela "A opcao foi 1" caso o programa receba 1 ou imprima "A opção foi 2" se o programa receber 2.

2\) Crie um programa que imprima o valor da soma se for um número acima de 5, caso não seja, imprima "Valor menor que 5".

