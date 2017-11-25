# Capítulo 15.2

## Gravação de arquivos de texto

###### Autora: [Maryana Feijó](https://github.com/maryfeijo)

---

###Introdução


Gravar dados em arquivos é realmente fácil, se você estiver acostumado com a func˜ao printf.
A função fprintf armazena dados em um arquivo. Seu funcionamento é muito semelhante ao printf, 
a diferença principal é a existência de um parâmetro para informar o arquivo onde os dados serão armazenados.

###Sintaxe

fprintf(nome_do_ponteiro_para_o_arquivo, “%s”,variavel_string)

Veja como se faz isso com esse exemplo simples:

#include <stdio.h>
#include <conio.h>
 
int main(void)
{
  FILE *pont_arq; // cria variável ponteiro para o arquivo
  char palavra[20]; // variável do tipo string
 
  //abrindo o arquivo com tipo de abertura w
  pont_arq = fopen("arquivo_palavra.txt", "w");
 
  //testando se o arquivo foi realmente criado
  if(pont_arq == NULL)
  {
     printf("Erro na abertura do arquivo!");
     return 1;
  }
 
  printf("Escreva uma palavra para testar gravacao de arquivo: ");
  scanf("%s", palavra);
 
  //usando fprintf para armazenar a string no arquivo
  fprintf(pont_arq, "%s", palavra);
 
  //usando fclose para fechar o arquivo
  fclose(pont_arq);
 
  printf("Dados gravados com sucesso!");
 
  getch();
  return(0);
}


###Referências

http://linguagemc.com.br/arquivos-em-c-categoria-usando-arquivos/
http://fig.if.usp.br/~esdobay/c/arquivos.pdf
http://www.cprogressivo.net/2013/11/Escrevendo-em-arquivos-As-funcoes-fputc-fprintf-fputs.html