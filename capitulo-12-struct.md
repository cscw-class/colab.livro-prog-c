# Capítulo 12: Struct

Aluno: Gabriel Amorim Rabello Sampaio - [**GitHub**](http://github.com/gabrielsampaio)

**1 - Definição **

Struct\(abreviatura de _structure_\) tem como ideia declara mais de um registro em uma só varivavel, assim uma só variavel poderia ter varias outras informações sobre uma mesma  informação.

**2 - Criando e manipulando**

Por exemplo, se fosse necessário armazenar 300 eventos com o dia e hora que irão acontecer. Seria assim sem utilizarmos struct:

```c
char evento[300][255];
char dia[300][10];
char hora[300][5];
```

Porém usando struct conseguimos definir que evento possui seu dia e hora:typedef struct { // Criamos a struct e definimos como um Tipo de variavel declaravel

```c
    char dia[10]; // Definimos que todo evento tem um campo dia de tamanho 10
    char hora[5]; // Definimos que todo evento tem um campo hora de tamanho 5
    char nome[255]; // Definimos que todo evento tem um campo nome de tamanho 255
} Evento; // Criamos o nome do tipo criado

// Declaramos uma variavel eventos do tipo evento com 300 eventos
Evento eventos[300];
Evento evento;

// Manipulariamos o conteudo dos eventos assim:
// Se quiseremos só um evento podemos usar assim:
evento.dia = "23/11/2017"; // Utilizando o "." conseguimos editar o item dia do evento 
evento.hora = "23:00";
evento.nome = "Two Moro Lente";


// E no caso de termos mais de um eventos, como é nosso exemplo, podemos utilizar um array de evento, assim cada index do array a partir do [0],[1],...,[300]
eventos[0].dia = "23/11/2017";
eventos[0].hora = "23:00";
eventos[0].nome = "Two Moro Lente";
```

**3 - Referências**

\[1\] -[  http://www.tiexpert.net/programacao/c/struct.php](http://www.tiexpert.net/programacao/c/struct.php)

\[2\] - [http://www.inf.pucrs.br/~pinho/LaproI/Structs/Structs.htm](http://www.inf.pucrs.br/~pinho/LaproI/Structs/Structs.htm)

