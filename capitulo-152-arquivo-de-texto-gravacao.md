## **15.2 – Arquivo Texto - Gravação**

**Autor: Matheus Simões Felix da Silva - **[**Github**](https://github.com/MathSimoes)

### **15.2.1 – bibliotecas **

Quando fornecemos dados por meio de um teclado, essas informações são passadas em série, por meio de stream, como se fosse um arquivo, embora este não exista. O programa em C vai ler esses dados do teclado COMO SE FOSSE um arquivo.

Isso ocorre porque ao criar um programa em C, estamos automaticamente usando alguns tipos de arquivos.

Mesmo que apenas tenhamos a interação teclado-programa-tela, existem alguns arquivos abertos, e os mais importantes são:

* stdin - é o arquivo de entrada padrão. Até o momento, para nós, foi o teclado.

* stdout - é o arquivo de saída padrão. Até o momento, nossa saída padrão é a tela do computador, através do terminal de comando.

* stderr - arquivo padrão de erro, onde podemos direcionar mensagens de erro para outro local sem ser o da saída padrão, como para um log \(espécie de registro de ações\)

Por isso, pode-se usar a vontade funções como printf, scanf, putc e outras.

Mas agora não vamos mais usar essas entradas e saídas padrão, e sim arquivos, por isso iremos fornecer algumas informações especiais aos nossos programas, informações sobre as entradas e saídas, que serão em formas de arquivos salvos na sua máquina.

### **15.2.2 – Gravar um caractere no arquivo**

Para escrever um caractere em um arquivo precisa-se usar a função fputc\(\), que recebe dois dados: o caractere e o FILE\*, que terá as informações do local onde iremos escrever o dito caractere:

`intfputc(int char, FILE *arq);`

Essa função retorna EOF caso não tenha conseguido escrever no arquivo, ou retorna o inteiro que representa o caractere, caso tenha ocorrido.

Inicialmente é preciso definir nosso endereço através de uma string \(char url\[\]\), que para explicação usaremos "char.txt", bem como o variável ch para armazenar o caractere que o usuário digitar.

Para salvar o char em um arquivo, criamos um ponteiro arq do tipo FILE.

```c
char url[] = "char.txt";
char ch;
FILE *arq;
```

Em seguida, pedimos para o usuário digitar algum caractere, que capturamos através da função getchar\(\) e salvamos em ch. Após abriremos um arquivo para escrever, e isso é feito através da função fopen\(\), que vai receber a string com a localização do arquivo \(isto está armazenado na variável url\) e o modo de abertura.

Como queremos escrever, o modo é o "w".

`arq = fopen(url, "w");`

Para checarmos se abertura do arquivo foi efetuada com êxito, testamos se a _fopen\(\)_ não retornou NULL para _arq_, caso não, segue o código para escrever o caractere no arquivo.

```c
if(arq==NULL){
    printf("Erro, nao foi possivel abrir o arquivo\n");
}else{
    fputc(ch, arq);
    fclose(arq);
}
```

Ao término é necessário fechar o arquivo, usando a função _fclose\(\)_ e passando o \_arq \_como argumento.

O código C ficou:

```c
#include<stdio.h>

int main(void) {
    char url[] = "char.txt";
    char ch;
    FILE *arq;

    printf("Caractere:");
    ch = getchar();
    arq = fopen(url,"w");

    if(arq==NULL){
        printf("Erro, nao foi possivel abrir o arquivo\n");
    }else{
        fputc(ch,arq);
        fclose(arq);
    }
    return 0;
}
```

Pronto, agora vá na pasta onde está localizado seu executável e vai ver que foi criado um arquivo chamado "char.txt", e dentro dele está o caractere que você digitou.

### **15.2.3 - Adicionando caractere com o modo "a" \(append\)**

Para escrever um texto em sequência, temos que alterar apenas uma coisa: o modo de abertura, de "w" para "a", assim sempre que escrevermos algo, será inserido ao final, anexando, em vez de substituir.

Após os passos do capítulo anterior, crie um looping DO WHILE onde nele, irá ser solicitado os caracteres ao usuário, e este laço só termina se digitarmos enter \(caractere '\n'\). Como a ideia é alterar várias vezes o arquivo, abrimos ele antes do looping e fechamos depois.

O código fica:

```c
#include<stdio.h>

int main(void) {

    char url[] = "char.txt";
    char ch;

    FILE *arq;
    arq = fopen(url, "a");

    if(arq == NULL){
        printf("Erro, nao foi possivel abrir o arquivo\n");
    } else {
        do{
            printf("Caractere:");
            ch = getchar();
            fflush(stdin);
            fputc(ch, arq);

        } while(ch != '\n');
    }
    fclose(arq);
    return 0;
}
```

Digite caractere por caractere, inclusive espaço, em seguida dê enter para terminar. Ao término é possível ver no arquivo a string escrita pela usuário.

## **15.2.4 - Escrevendo textos \(strings\) em arquivos**

Para escrever mais de um caractere existe a função _fprintf_, que nos permite escrever strings inteiras em arquivos.Sua sintaxe simplificada é:

```c
int fprintf(FILE *arq, char string[])
```

Ou seja, recebe o local onde deve direcionar a saída \(para um arquivo, apontado pelo ponteiro \_arq \_do tipo FILE\), e a string que devemos adicionar em tal arquivo. Essa função retorna EOF em caso de erro.

Inicialmente definir a nossa url como "teste.txt" e criar um vetor de char para armazenar a palavra ou frase. A cada vez que o usuário informar uma letra ele será pego pelo método _gets\(\)_ e cada caractere armazenado em uma posição do vetor.

```c
gets(nome);
```

Em seguida, verificaremos se de fato ocorreu a abertura do arquivo, caso o arquivo tenha sido aberto corretamente o programa solicitará a palavra ou frase que o usuário deseja gravar em arquivo.

```c
if ((fp=fopen (“teste.txt”,"w")) != NULL) {
    for(int i=0; i<10; i++) {
        printf(“Escreva um nome: ”);
        gets(nome);
        fprintf(fp, “Nome %d: %s\n”, i+1, nome);
    }
}
```

Ao término deve-se lembrar de fechar o arquivo alterado utilizando o método _fclose\(\)_.

```c
fclose(arq);
```

Veja como ficou o código:

```c
#include<stdio.h>

int main(void) {
    FILE *arq;
    char nome[50];
    if ((fp=fopen (“teste.txt”,"w")) != NULL) {
        for(int i=0; i<10; i++) {
            printf(“Escreva um nome: ”);
            gets(nome);
            fprintf(fp, “Nome %d: %s\n”, i+1, nome);
        }
    }
    fclose(arq);
    return 0;
}
```

Ao término da execução do programa é possível ver o arquivo dentro da pasta de onde esta localizado o programa executado.



**          
**

