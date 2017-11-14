### Capítulo 7.1: For

O comando For é uma estrutura de repetição. A estrutura de repetição permite que uma instrução seja executada mais de uma vez em um programa. Uma variável deve ser inicializada para controlar os loops \(voltas\). O comando for, é formado por três condições, que são compostas pela inicialização, referente ao valor inicial atribuída para a variável; a condição, na qual é avaliada e se for verdadeira, os comandos do bloco são executados, senão o loop é encerrado e o incremento, na qual é somada, na variável, um determinado valor, escolhida pelo usuário.

##### 

No exemplo abaixo mostra a sintaxe básica do comando For:

```
     Exemplo 1:

     for ( inicialização; condição; incremento )
     {
         sequência de comandos;
     }
```

Neste segundo exemplo , é mostrado um código de impressão na tela do número 1 até 10 , utilizando o comando For.  A variável número é inicializada como um valor inteiro . Dentro do comando For, em sua primeira condição: numero =1, a variável numero vai recebeu1 como valor. Na segunda condição; numero &lt;= 10, o programa vai repetir a condição a instrução: cout &lt;&lt; "Numero:" &lt;&lt; numero &lt;&lt; endl; enquanto o número for menor ou igual a dez, mostrando na tela os números, na terceira condição: numero++, será somado +1 no valor da variável, quando a variável número chegar em 11, o programa não vai mais executar a instrução, saindo do loop.

```
    Exemplo 2:

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

No terceiro exemplo, mostra a utilização do comando For, para determinar quantidade e vezes ele vai se repetir.

```
   Exemplo 3:

   #include<iostream>;
   using namespace std;

   main(void)
   {
      int numero;
      int quantasVezes;
      char nome[7];
      int idade;

      cout << "Quantas vezes repetir?";
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

O usuário deve escolher quantas vezes o comando for irá repetir as suas instruções então se o usuário digitar 5, por exemplo, ele deve digitar, um nome e uma idade, cinco vezes, que serão impressas na tela. A imagem abaixo mostra um exemplo de impressão na tela:

![](/assets/exemplo_for.PNG)

No quarto exemplo, mostra o cálculo de uma soma dos elementos de 1 até 10.

```
 Exemplo 4:

 #include <stdio.h>
 #include<stdlib.h>
 int main()
 {
    int i,s=0;
    for(i=0; i<=10; i++)
    {
        s = s + 1;
    }
    cout << "Soma= %d\n",s;
 }
```

##### 

##### Lista de Exercícios:

1\) Faça uma contagem regressiva, de 10 até 1, utilizando o comando for.

##### Referências:

O comando for em C, Disponível em: &lt;http://linguagemc.com.br/a-estrutura-de-repeticao-for-em-c/&gt;. Acesso em 12/11.

Estrutura de repetição: C++, Disponível em: &lt;https://www.devmedia.com.br/estrutura-de-repeticao-c/24121&gt;.Acesso em: 12/11

Comando For: - Java, C++, e C\#, Disponível em: https://desenvolvimentoaberto.org/2014/01/30/comando-for-java-c-e-c/&gt; .Acesso em: 12/11



