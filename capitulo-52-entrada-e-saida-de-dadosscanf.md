# **Capítulo 5.2 - Entrada e saida de dados scanf**

##### **Autor: Matheus Ferreira dos Santos - **[Github](https://www.gitbook.com/book/alexsalgado/introducao-a-programacao-em-c/edit#)

#### **Definição:**

###### **A função scanf funciona de maneira semelhante ao printf. É uma das funções de E/S implementadas em todos os compiladores e nos permite ler dados formatados da entrada padrão \(teclado\).**

###### **Sintaxe:**

###### **scanf\(“expressão de controle”, lista de argumentos\);**

###### **A lista de argumentos deve consistir nos endereços das variáveis que irão armazenar os valores lidos. C possui um operador para tipos básicos chamado operador de endereço e referenciado pelo símbolo '&' que fornece o endereço do operando.Toda variável ocupa uma certa localização na memória, e seu endereço é o do primeiro byte ocupado por ela. Um erro muito comum de programadores que usam a função scanf é esquecer de utilizar o caractere “E comercial” \(&\) antes do nome da variável que deve receber o valor convertido a partir dos caracteres do fluxo de entrada!**

###### **A tabela abaixo mostra os códigos de formatação da função scanf\(\)**

###### **Código Significado**

###### **%c caracter simples**

###### **%d inteiro decimal**

###### **%e notação científica**

###### **%f ponto flutuante**

###### **%o inteiro octal**

###### **%s cadeia de caracteres**

###### **%u decimal sem sinal**

###### **%x hexadecimal**

###### **%l inteiro longo**

###### **%lf double**

#### **Exemplos:**

###### **• Um inteiro ocupa 2 bytes. Se você declarou a variável n como inteira a atribuiu a ela o valor 2, quando n for referenciada devolverá 2. Entretanto, se você referenciar n precedido de & \(&n\) devolverá o endereço do primeiro byte onde n está armazenada.**

###### **• Vamos escrever um programa em C que pede um número ao usuário e o mostra na tela:**

###### **\#include &lt;stdio.h&gt;**

###### **int main\(\){**

###### **int numero;**

###### **printf\("Digite um numero: "\);**

###### **scanf\("%d", №\);**

###### **printf\("O numero digitado foi: %d", numero\);**

###### **}**

**Fontes:**

[**http://www.cprogressivo.net/2012/12/A-funcao-scanf-recebendo-numeros-do-usuario.html**](https://www.gitbook.com/book/alexsalgado/introducao-a-programacao-em-c/edit#)

[**https://edisciplinas.usp.br/pluginfile.php/3169937/mod\_resource/content/0/Material Complementar bsicos.pdf**](https://www.gitbook.com/book/alexsalgado/introducao-a-programacao-em-c/edit#)

[**http://homepages.dcc.ufmg.br/~rodolfo/aedsi-2-10/printf\_scanf/printfscanf.html**](https://www.gitbook.com/book/alexsalgado/introducao-a-programacao-em-c/edit#)

  


