# **16.2 Arquivo Binário - Gravação**



Por: **João Victor Tavares**  


### 1- Como iniciar uma gravação **Gravação**

   Para gravação de arquivos texto usa-se a função  **fwrite**.

* **Exemplo de fwrite:**
* // \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
* //  Exemplo de uso de arquivo binário
* //  Este programa grava um vetor em um arquivo binário
* //
* // \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
* \#include &lt;stdio.h&gt;
* void main\(\)
* {
*     double Notas\[100\];      FILE \*arq;      int result;      int i;
*     arq = fopen\("ArqTeste.dat", "wb"\); // Cria um arquivo binário para gravação 
* *      if \(arq == NULL\) // Se não conseguiu criar
*     {
*         printf\("Problemas na CRIACAO do arquivo\n"\);
*  return;
*  }
*     // Grava 30 números do vetor a partir da posição 50 
*     result = fwrite \(&Notas\[50\], sizeof\(double\), 30, arq\);
* *     printf\("Nro de elementos gravados: %d", result\); 
*     fclose\(arq\);
* }

## 2- Valores modo válidos

#### 

#### fopen

Esta é a função de abertura de arquivos. Seu protótipo é:

```
                FILE *fopen (char *nome_do_arquivo,char *modo);
```

O nome\_do\_arquivo determina qual arquivo deverá ser aberto. Este nome deve ser válido no sistema operacional que estiver sendo utilizado. O modo de abertura diz à função**fopen\(\)**que tipo de uso você vai fazer do arquivo. A tabela abaixo mostra os valores de modo válidos:  


| **Modo** | **Significado** |
| :--- | :--- |
| "r" | Abre um arquivo texto para leitura. O arquivo deve existir antes de ser aberto. |
| "w" | Abrir um arquivo texto para gravação. Se o arquivo não existir, ele será criado. Se já existir, o conteúdo anterior será destruído. |
| "a" | Abrir um arquivo texto para gravação. Os dados serão adicionados no fim do arquivo \("append"\), se ele já existir, ou um novo arquivo será criado, no caso de arquivo não existente anteriormente. |
| "rb" | Abre um arquivo binário para leitura. Igual ao modo "r" anterior, só que o arquivo é binário. |
| "wb" | Cria um arquivo binário para escrita, como no modo "w" anterior, só que o arquivo é binário. |
| "ab" | Acrescenta dados binários no fim do arquivo, como no modo "a" anterior, só que o arquivo é binário. |
| "r+" | Abre um arquivo texto para leitura e gravação. O arquivo deve existir e pode ser modificado. |
| "w+" | Cria um arquivo texto para leitura e gravação. Se o arquivo existir, o conteúdo anterior será destruído. Se não existir, será criado. |
| "a+" | Abre um arquivo texto para gravação e leitura. Os dados serão adicionados no fim do arquivo se ele já existir, ou um novo arquivo será criado, no caso de arquivo não existente anteriormente. |
| "r+b" | Abre um arquivo binário para leitura e escrita. O mesmo que "r+" acima, só que o arquivo é binário. |
| "w+b" | Cria um arquivo binário para leitura e escrita. O mesmo que "w+" acima, só que o arquivo é binário. |
| "a+b" | Acrescenta dados ou cria uma arquivo binário para leitura e escrita. O mesmo que "a+" acima, só que o arquivo é binário |

Poderíamos então, para abrir um arquivo binário para escrita, escrever:

```
FILE *fp;		/* Declaração da estrutura
fp=fopen ("exemplo.bin","wb");  /* o arquivo se chama exemplo.bin e está localizado no diretório corrente */
if (!fp)
        printf ("Erro na abertura do arquivo.");
```

A condição**!fp**testa se o arquivo foi aberto com sucesso porque no caso de um erro a função**fopen\(\)**retorna um ponteiro nullo \(**NULL**\). 

Uma vez aberto um arquivo, vamos poder ler ou escrever nele utilizando as funções que serão apresentadas nas próximas páginas.

Toda vez que estamos trabalhando com arquivos, há uma espécie de posição atual no arquivo. Esta  é a posição de onde será lido ou escrito o próximo caractere. Normalmente, num acesso sequencial a um arquivo, não temos que mexer nesta posição pois quando lemos um caractere a posição no arquivo é automaticamente atualizada. Num acesso randômico teremos que mexer nesta posição \(ver[fseek\(\)](http://www.pucsp.br/~so-comp/cursoc/aulas/c970.html)\).

#### exit

Aqui abrimos um parênteses para explicar a função**exit\(\)**cujo protótipo é:

```
                void exit (int codigo_de_retorno);
```

Para utilizá-la deve-se colocar um include para o arquivo de cabeçalho stdlib.h. Esta função aborta a execução do programa. Pode ser chamada de qualquer ponto no programa e faz com que o programa termine e retorne, para o sistema operacional, o código\_de\_retorno. A convenção mais usada é que um programa retorne zero no caso de um término normal e retorne um número não nulo no caso de ter ocorrido um problema. A função**exit\(\)**se torna importante em casos como alocação dinâmica e abertura de arquivos pois nestes casos, se o programa não conseguir a memória necessária ou abrir o arquivo, a melhor saída pode ser terminar a execução do programa. Poderíamos reescrever o exemplo da seção anterior usando agora o exit\(\) para garantir que o programa não deixará de abrir o arquivo:

```
#include 
<
stdio.h
>

#include 
<
stdlib.h
>
 /* Para a função exit() */
main (void)
{
FILE *fp;
...
fp=fopen ("exemplo.bin","wb");
if (!fp)
        {
        printf ("Erro na abertura do arquivo. Fim de programa.");
        exit (1);
        }
...
return 0;
}
```

#### fclose

Quando acabamos de usar um arquivo que abrimos, devemos fechá-lo. Para tanto usa-se a função**fclose\(\)**:

```
                int fclose (FILE *fp);
```

O ponteiro**fp**passado à função**fclose\(\)**determina o arquivo a ser fechado. A função retorna zero no caso de sucesso.

Fechar um arquivo faz com que qualquer caracter que tenha permanecido no "buffer" associado ao fluxo de saída seja gravado. Mas, o que é este "buffer"? Quando você envia caracteres para serem gravados em um arquivo, estes caracteres são armazenados temporariamente em uma área de memória \(o "buffer"\) em vez de serem escritos em disco imediatamente. Quando o "buffer" estiver cheio, seu conteúdo é escrito no disco de uma vez. A razão para se fazer isto tem a ver com a eficiência nas leituras e gravações de arquivos. Se, para cada caracter que fossemos gravar, tivéssemos que posicionar a cabeça de gravação em um ponto específico do disco, apenas para gravar aquele caracter, as gravações seriam muito lentas. Assim estas gravações só serão efetuadas quando houver um volume razoável de informações a serem gravadas ou quando o arquivo for fechado.

A função[exit\(\)](http://www.pucsp.br/~so-comp/cursoc/aulas/c950.html#c952)fecha todos os arquivos que um programa tiver aberto.







  




