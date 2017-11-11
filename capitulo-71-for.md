### **Capítulo 7.1: For**

##### O comando For é uma estrutura de repetição. A estrutura de repetição permite que uma instrução seja executada mais de uma vez em um programa. Uma variável deve ser inicializada para controlar os loops \(voltas\). O comando For, é formado por três condições, que são compostas pela inicialização, referente ao valor inicial atribuída para a variável; a condição, na qual é avaliada e se for verdadeira, os comandos do bloco são executados, senão o loop é encerrado e o incremento, na qual é somada, na variável, um determinado valor, escolhida pelo usuário.

##### 

##### No exemplo abaixo mostra a sintaxe básica do comando For**:**

```
     for ( inicialização; condição; incremento )
     {
         sequência de comandos;
     }
```

##### Neste segundo exemplo, é mostrado um código de impressão na tela do número 1 até 10, utilizando o comando For: A variável número é inicializada como um valor inteiro. Dentro do comando For, em sua primeira condição: numero =1, a variável número vai receber 1 como valor. Na segunda condição: numero&lt;=10, o programa vai repetir a instrução: cout &lt;&lt; " Número...:" &lt;&lt; numero &lt;&lt; endl; enquanto o número for menor ou igual a dez, mostrando na tela os números, na terceira condição: numero ++, será somado +1 no valor da variável número e quando chegar ao valor 11 o programa não vai mais executar a instrução, saindo do loop.

##### No terceiro exemplo mostra a utilização do comando For para determinar a quantidade de vezes que o comando For se repetirá.

```
    #include <iostream>
    using namespace std;
    main (void)
    {

       int numero;   
       for ( numero=1; numero;<=10; numero++)
       {
           cout << "Numero:"  << numero << endl;
       }
     }
```

##### No terceiro exemplo, mostra a utilização do comando For, para determinar quantidade e vezes ele vai se repetir.

```
  #include<iostream>;
  using namespace std;

  main(void)
  {
      int numero;
      int quantasVezes;
      char nome[7];
      int idade;

      cout << Quantas vezes repetir? ";
      cin >> quantasVezes;

      for( numero=1; numero<=quantasVezes; numero++)
      {
         cout << "Digite um nome:";
         cin >> nome;

         cout << "Digite uma idade:";
         cin >> idade;
      }
   }
```

##### O programa pergunta para o usuário quantas vezes ele quer repetir o comando For. A resposta do número de vezes, será armazenada na variável quantasVezes, então se a resposta foi 5, o programa vai perguntar o nome e a idade e imprimir na tela, quatro vezes.

##### Exemplo do resultado da impressão na tela deste código:

![](/assets/exemplo_for.PNG)

\#include&lt;iostream&gt;



#### 

#### 

#### 

#### Usando o Foreach\(\):

##### O Foreach tem o mesmo funcionamento do For, porém ele não precisa de contador, ele executa um grupo de comandos para cada elemento de um array, por exemplo:



##### Exercícios:



