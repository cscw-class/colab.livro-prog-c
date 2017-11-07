# Capítulo 6.2: Tomada de Decisões - Switch

##### **Autor: **[**Ian Saud Soares**](https://github.com/iansaud)** **

#### Introdução

          Basicamente Switch é um mecanismo para reduzir a utilização de diversos IF's e Else's o quer permitem diversas linhas de execução de código mediante uma condição. Com isso reduz a complexidade e facilita e muito entendimento da sua linha de código, é muito utilizado também para criação de menus em C/C++.

#### Algorítmo/Pseudocódigo

```c
possibilidade (variavel ou valor)
// Determina o Inicio
{
    caso (X): // Onde caso a variavel inserida anteriormente tenha valor igual a este, ele irã realizar a ação abaixo
    // Realiza uma ação
    caso (Z): // Onde caso a variavel inserida anteriormente tenha valor igual a este, ele irã realizar a ação abaixo
    // Realiza uma Ação

}
// Determina o Fim
```

Neste exemplo acima, podemos analisar que quando o compilador acessa o caso Switch, ele necessita de uma variável á  ser passada como parâmetro, esta que será comparada aos valores abaixo para entrar em cada situação listada abaixo.

#### Codigo utilizando If's Else's

```c
if (valor == X)
    // Realiza Ação
else
    if (valor == Z)
        //Realiza Ação
    else
        if (valor == Y)
            //Realiza Ação
```

Neste segundo exemplo utilizando If's e Else's encadeados podemos notar que o código fica bem mais complexo e cansativo para o leitor.

#### Código Utilizando Switch

```
switch (valor)
{
    case valor1:
        //Realiza Ação
    break;
    case valor2:
        //Realiza Ação
    break;
    case valor3:
        //Realiza Ação
    break;
}
```

Também podemos definir uma ação padrão\(default\) para caso o valor passado não seja igual a nenhum dos cases



