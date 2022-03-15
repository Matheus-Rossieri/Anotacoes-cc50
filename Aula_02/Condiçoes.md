## **Condições**

Podemos traduzir condições, ou blocos “se”, com:

```
if (x < y)
{
     printf (“x é menor que y\n”); 
}
```

- Observe que em C, usamos **{** e **}** (bem como indentação) para indicar como as linhas de código devem ser aninhadas.

Podemos ter condições “if” e “else”:

```
if (x < y)
{
     printf(“x é menor que y\n”); 
}
else
{
    printf(“x não é menor que y\n”); 
}
```

E até mesmo “senão se(else if)”:

```
if (x < y)
{
     printf(“x é menor que y\n”); 
}
else if (x > y)
{
    printf(“x é maior que y\n”); 
}
else if (x == y)
{
    printf(“x é igual a y\n”); 
}
```

- Observe que, para comparar dois valores em C, usamos **==**, dois sinais de igual.
- E, logicamente, não precisamos de `if (x == y)` na condição final, já que esse é o único caso restante, então podemos apenas dizer o contrário com **else**:

```
if (x < y)
{
     printf(“x é menor que y\n”); 
}
else if (x > y)
{
    printf(“x é maior que y\n”); 
}
else
{
    printf(“x é igual a y\n”); 
}
```

Vamos dar uma olhada em outro exemplo, **conditions.c**:

```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
     // Usuário entra com o valor de x
     int x = get_int(“x: “);

     // Usuário entra com o valor de y
     int y = get_int(“y: “);

     // Compara x e y
     if (x < y)
     {
         printf(“x é menor que y\n”); 
     }
     else if (x > y)
     {
        printf(“x é maior que y\n”); 
     }
     else
     {
        printf(“x é igual a y\n”); 
     }
}
```

- Nós incluímos as condições que acabamos de ver, juntamente com duas “chamadas”, ou usos, de get_int para obter x e y do usuário.
- Vamos compilar e executar nosso programa para ver se ele realmente funciona conforme o planejado.

Em **concorda.c**, podemos pedir ao usuário para confirmar ou negar algo:

```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
     // Solicita um caracter para o usuário
     char c = get_char("Você concorda?");

     // Verifica se concordou
     if (c == ‘S’ || c == ‘s’)
     {
         printf(“Concordo.\n”); 
     }
     else if (c == ‘N’ || c == ‘n’)
     {
        printf(“Não concordo..\n”); 
     }
}
```

- Com **get_char**, podemos obter um único caractere e, como só temos um em nosso programa, parece razoável chamá-lo de **c**.
- Usamos duas barras verticais, **||** , para indicar um “ou” lógico (matematico), onde qualquer uma das expressões pode ser verdadeira para que a condição seja seguida. (**&&**, por sua vez, indica um “e” lógico, onde ambas as condições deveriam ser verdadeiras.) E observe que usamos dois sinais de igual, **==** , para comparar dois valores, bem como aspas simples, **’**, para envolver nossos valores de caracteres únicos.
- Se nenhuma das expressões for verdadeira, nada acontecerá, pois nosso programa não tem um loop.
