## **Mario**Podemos querer um programa que imprima parte de uma tela de um videogame como Super Mario Bros. Em **mario.c**, podemos imprimir quatro pontos de interrogação, simulando blocos:

```
#include <stdio.h>

int main(void)
{
     printf(“?????\n”); 
}
```

Com um loop, podemos imprimir vários pontos de interrogação, seguindo-os com uma única nova linha após o loop:

```
#include <stdio.h>

int main(void)
{
     for(int i = 0; i < 3; i++)
     {  
           printf(“?”); 
     }
     printf (“\n”); 
}
```

Podemos obter um número inteiro positivo do usuário e imprimir esse número de pontos de interrogação, usando **n** para o nosso loop:

 

```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
     //  Pega o valor de n com o usuário
    int n;
    do
    {
          n = get_int(“Largura: “);
    }
    while (n < 1);

    // Imprima pontos de interrogação 
    for(int i = 0; i < n; i++)
    {
         printf(“?”); 
    }
    printf(“\n”); 
}
```

E podemos imprimir um conjunto bidimensional de blocos com loops aninhados, um dentro do outro:

```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    for(int i = 0; i < 3; i++)
    {
	    for(int j = 0; j < 3; j++)
    	{
         		printf(“#”); 
    	}
    	printf(“\n”); 
    }
}
```

- Temos dois loops aninhados, onde o loop externo usa **i** para fazer tudo que contem 3 vezes, e o loop interno usa **j** , uma variável diferente, para fazer algo 3 vezes para cada um desses tempos. Em outras palavras, o loop externo imprime 3 linhas, terminando cada uma delas com uma nova linha, e o loop interno imprime 3 colunas, ou caracteres tipo **#**, *sem* uma nova linha.
