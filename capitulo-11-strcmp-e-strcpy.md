# **Strcmp**

Compara o conteúdo de duas strings;

Pode apresentar os seguintes retornos:

* 0: conteúdo das strings são iguais

* &lt; 0: conteúdo da string1 é menor do que string2

* &gt; 0: conteúdo da string1 é maior do que string2

### Exemplo de programa usando strcmp:

```
#include <stdio.h>
#include <string.h>
```

```
int main ()
{
    char str1[100],str2[100];
    printf ("Entre com uma string: ");
    gets (str1);
    printf ("\n\nEntre com outra string: ");
    gets (str2);
    if (strcmp(str1,str2))
            printf ("\n\nAs duas strings são diferentes.");
    else printf ("\n\nAs duas strings são iguais.");
    return(0);
}
```

# **Strcpy**

strcpy\(string\_destino, string\_origem\);

Realiza a cópia do conteúdo de uma variável a outra.

### Exemplo de programa usando Strcpy:

```
#include <stdio.h> 
#include<string.h>
```

```
int main ()
{
    char str1[100],str2[100],str3[100];
    printf ("Entre com uma string: ");
    gets (str1);
    strcpy (str2,str1);    /* Copia str1 em str2 */
    strcpy (str3,"Voce digitou a string "); /* Copia "Voce digitou a string" em str3 */
    printf ("\n\n%s%s",str3,str2);
    return(0);
}
```

**Referências**:

[http://www.facom.ufu.br/~madriana/PP/TP6.pdf](http://www.facom.ufu.br/~madriana/PP/TP6.pdf)

[http://mtm.ufsc.br/~azeredo/cursoC/aulas/c520.html](http://mtm.ufsc.br/~azeredo/cursoC/aulas/c520.html)

[http://linguagemc.com.br/a-biblioteca-string-h/](http://linguagemc.com.br/a-biblioteca-string-h/)

