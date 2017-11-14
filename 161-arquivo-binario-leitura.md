## Capítulo 16.1: Leitura de Arquivo Binário

_**Por Renan Xavier Calmon - **_[_**Github**_](https://github.com/Renanxc)

#### 16.1.1 - Manipulação de arquivos

Para utilizar-se das funções de manipulação de arquivo, primeiramente deve-se incluir a biblioteca &lt;**STDIO.H**&gt;. Logo deverá abrir o arquivo utilizando-se do comando **fopen**, que deverá retornar um "apontador" ou **NULL**. Necessitando um ponteiro para receber o endereço do arquivo:

_Exemplo:_

> FILE \*arq;
>
> arq = fopen\("arquivo.dat", "rb"\);
>
> if \(arq == NULL\){
>
> ```c
> printf\("Problemas na abertura do arquivo\n"\);
> system("pause");
> exit(1);
> ```
>
> }

O primeiro parâmetro é o nome do arquivo, o segundo a forma de abertura, sendo "wb" abertura para gravação de arquivos do binário e "rb" para leitura.

#### 16.1.2 - Leitura de arquivo binário

Para a leitura de arquivo, utilizaremos o comando **fread:**

> fread \(void \*buffer, int numero\_de\_bytes, int count, FILE \*fp\);

O buffer é a região de memória na qual serão armazenados os dados lidos. O número de bytes é o tamanho da unidade a ser lida. count indica quantas unidades devem ser lidas.

A função retorna o número de unidades efetivamente lidas. Este número pode ser menor que count quando o fim do arquivo for encontrado ou ocorrer algum erro. Quando o arquivo for aberto para dados binários, fread pode ler qualquer tipo de dados.

_Exemplo:_

> \#include &lt;stdio.h&gt;
>
>  \#include &lt;stdlib.h&gt;
>
> int main\(\) {
>
> > FILE \*pf;
> >
> > char conteudo\[100\];
> >
> > pf = fopen\("arquivos/texto.bin","rb"\);
> >
> > fread\(&conteudo,sizeof\(char\),100,pf\);
> >
> > printf\("\nO conteúdo do arquivo é':\n%s\n",conteudo\);
> >
> > fclose\(pf\);
> >
> > return\(0\);
>
> }



