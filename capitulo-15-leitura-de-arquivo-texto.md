## **15.1 - Leitura de arquivos utilzando a linguagem C.**



Para leitura de arquivos utilizando a linguagem C existem duas funções já implementadas pela biblioteca "stdio.h", a fgets e fscanf. Ambas as funções precisam que haja um ponteiro com o endereço do arquivo que deve ser lido, logo o arquivo deve ser aberto, como mostrado no exemplo1.



`//Exemplo1: `

`arq = fopen("ArqTeste.txt", "rt");`



Neste exemplo 'arq' é o ponteiro que armazenará o endereço do para a leitura, 'fopen' é a função responsável pela abertura do aquivo e 'ArqTeste.txt' o nome do arquivo, ou o endereço para o mesmo, e "rt" indica a função fopen que este arquivo será utilizado para a leitura de um arquivo do tipo texto.

### 15.1.1 - Leitura com FGETS



A função "fgets" lê linha a linha a linha inteira, ou seja, até que encontra o caracter '\n', que indica o fim da string, podendo ser passado também o numero de caracteres para serem lidos.



`//Exemplo2: `

`result = fgets(Linha, 100, arq);`



No exemplo2 um a função 'fgets' lê até 99 caracteres ou até encontrar '\n', 'arq' representa o ponteiro para o arquivo que será lido, e 'Linha' é o vetor que deverá armazenar a string e 'result' receberá o o endereço em caso de sucesso ou 'NULL' em caso de falha.



Se a função for executado sem apresentar nenhum problema irá retornar o inicio do endereço da string lida, caso haja algum problema será retornado valor nulo \(este é o valor recebido por 'result'\).

### 15.1.2 - Leitura com FSCANF

A função 'fscanf' funciona exatamente como função 'scanf mas lendo os dados diretamento do arquivo ou invés de esperar uma entrada pelo teclado.



`//Exemplo3: `

`result = fscanf(arq, "%d%f", &i, &x);`



No exemplo3 'arq' representa o ponteiro para o arquivo que será lido, '%d%f' irá armazenar os valores de um inteiro e um float \(exatamente como no 'scanf'\), &i é a variavel de tipo inteiro, &x é uma variavel de tipo float.

Se o valor de 'result' for igual à constante 'EOF', o arquivo chegou ao fim.

### 15.1.3 - Considerações.



Cada uma destas funções pode ser utilizada em situações diferentes para uma leitura mais precisa e adequada em cada tipo de situação. Como por exemplo para lermos uma texto utilizando a função fscanf teriámos que ler caracter a caracter, já para lermos um numeral com fgets teriamos que converte-lo para numeral, pois seria lido como um char. Sendo assim cada função tem sua melhor utilização.

