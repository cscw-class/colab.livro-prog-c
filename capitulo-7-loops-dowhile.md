# **Capítulo 7 : Loops While e Do-While**

**Por Jordan Mendonça**

Os comandos de repetição são um recurso que permite que um certo trecho do código de um programa seja **repetido** um certo número de vezes.

Na liguagem C existem dois comandos de repetição que se chamam While e Do-while.

## Comando while

O comando

**while**

permite que um certo trecho de programa seja executado

**ENQUANTO**

uma certa condição for

**verdadeira**

. A forma do comando

**while**

é a seguinte:

> > while \(condição\)  
> >    
> > {  
> >    
> > // comandos a serem repetidos  
> >    
> > // comandos a serem repetidos  
> >    
> > }  
> >    
> > // comandos após o 'while'

O funcionamento é o seguinte:

1. Testa a condição;
2. Se a  
   **condição**
    for 
   **falsa**
    então pula todos os comandos do bloco subordinado ao 
   **while**
    e passa a executar os comandos após o bloco do 
   **while**
   .
3. Se  
   **condição**
    for 
   **verdadeira**
    então executa cada um dos comandos do bloco subordinado ao 
   **while**
   .
4. Após executar o último comando do bloco do 
   **while**
    volta ao passo 1.

O comando

**while**

deve ser usado sempre que:

* **não soubermos exatamente quantas vezes o laço deve ser repetido**
  ;
* o teste deva ser feito 
  **antes de iniciar**
  a execução de um bloco de comandos;
* houver casos em que o laço 
  **não deva ser repetido nenhuma vez**
  .

### Exemplos

| int continua, contador;continua = 's'; contador = 0;while \(continua == 's'\)  // enquanto for igual a 's' { // comandos a serem repetidos   printf\("Repentindo....\n"\);   contador = contador + 1;   printf\("Tecle 's' se deseja continuar\n"\);    continua = getch\(\); }if \(contador == 0\) printf\("O bloco NAO foi repetido."\); else printf\("O bloco foi repetido %d vezes", contador\); |
| :--- |


| // Programa que calcula a idade média de um grupo de pessoas. // A finalização da entrada de números é dada por um -1int soma, quantidade, idade;float media;soma = 0; quantidade = 0;  idade = 0;while \(idade != -1\)  { // comandos a serem repetidos   printf\("Idade da pessoa %d. \(tecle -1 se quiser encerrar\).\n",                quantidade+1\);    scanf\("%d", &idade\);   if \(idade &gt;=0\)    {       soma = soma + idade;      quantidade = quantidade + 1;    } }// Faz o calculo da media de idadeif \(quantidade &gt;0\) {    media = \(float\) soma / quantidade;    printf\("A media de idade das %d pessoas eh: %5.2f", quantidade,             media\); } else printf\("Nenhum dado foi informado."\); |
| :--- |


### Observação:

Tenha atenção especial com o teste do comando while. As variáveis usadas no teste devem ter sido inicializadas

**antes do teste**

---

## Comando do-while

O comando

**do-while**

permite que um certo trecho de programa seja executado

**ENQUANTO**

uma certa condição for

**verdadeira**

. A forma do comando

**do-while**

é a seguinte:

> > do  
> >    
> > {  
> >    
> > // comandos a serem repetidos  
> >    
> > // comandos a serem repetidos  
> >    
> > } while \(condição\)  
> > ;  
> > // comandos após o 'do-while'

O funcionamento é o seguinte:

1. Executa os comando dentro do bloco 
   **do-while**
   ;
2. Testa a condição;
3. Se a  
   **condição**
    for 
   **falsa**
    então executa o comando que está logo após o bloco subordinado ao 
   **do-while**
    .
4. Se  
   **condição**
    for 
   **verdadeira**
    então volta ao passo 1.

O comando

**do-while**

deve ser usado sempre que:

* **que não soubermos exatamente quantas vezes o laço deve ser repetido**
  ;
* o teste deva ser feito 
  **depois da execução**
  de um bloco de comandos;
* o bloco de comandos deve se 
  **executado pelo menos 1 vez;**

### Exemplos

| int continua, contador;contador = 0; // nao precisamos inicializar a variável 'continua' pois o teste é feito  // depoisdo  { // comandos a serem repetidos   printf\("Repentindo....\n"\);   contador = contador + 1;   printf\("Tecle 's' se deseja continuar\n"\);    continua = getch\(\); } while \(continua == 's'\) printf\("O bloco foi repetido %d vezes", contador\); |
| :--- |


| // Programa que calcula a idade média de um grupo de pessoas. // A finalização da entrada de números é dada por um -1int soma, quantidade, idade;float media;soma = 0; quantidade = 0; do {      printf\("Idade da pessoa %d. \(tecle -1 se quiser encerrar\).\n",                quantidade+1\);      scanf\("%d", &idade\);     if \(idade &gt;=0\)      {         soma = soma + idade;        quantidade = quantidade + 1;      }    } while \(idade != -1\);// Faz o calculo da media de idadeif \(quantidade &gt; 0\) {    media = \(float\) soma / quantidade;    printf\("A media de idade das %d pessoas eh: %5.2f", quantidade,             media\); } else printf\("Nenhum dado foi informado."\); |
| :--- |




