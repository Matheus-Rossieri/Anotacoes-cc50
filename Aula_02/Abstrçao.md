## **Abstração**

Podemos escrever um programa que imprime **miau**(meow) três vezes:

```
#include <stdio.h>

int main(void)
{
     printf(“miau.\n”); 
     printf(“miau.\n”); 
     printf(“mmiau.\n”); 
}
```

Poderíamos usar um loop **for**, para não ter que copiar e colar tantas linhas:

```
#include <stdio.h>

int main(void)
{
     for(int i = 0; i < 3; i++)
     {
          printf(“miau.\n”); 
          printf(“miau.\n”); 
          printf(“miau.\n”); 
	 }
}
```

Podemos mover a linha **printf** para sua própria função, como nossa própria peça de quebra-cabeça:

```
#include <stdio.h>

void miau(void)
{
    printf(“miau.\n”); 
}

int main(void)
{
     for(int i = 0; i < 3; i++)
     {
         miau();
	 }
}
```

- Definimos uma função, **miau**, acima de nossa função principal(main).

Mas, convencionalmente, nossa **função principal**(main) deve ser a primeira função em nosso programa, então precisamos de mais algumas linhas:

```
#include <stdio.h>

void miau(void);

int main(void)
{
     for(int i = 0; i < 3; i++)
     {
          miau();
	 }
}

void miau(void)
{
      printf(“miau.\n”); 
}
```

- Acontece que precisamos declarar nossa função **miau** primeiro com um **protótipo**, antes de usá-lo em ***main\*** , e realmente defini-lo depois. O compilador lê nosso código-fonte de cima para baixo, então ele precisa saber que o **miau** existirá posteriormente no arquivo.

Podemos até mesmo alterar nossa função de **miau** para obter alguma entrada, **n** e miau **n** vezes:

```
#include <stdio.h>

void miau(int n);

int main(void)
{
     miau(3);
}

void miau(int n)
{
     for(int i = 0; i < 3; i++)
     {
          printf(“miau.\n”); 
	 }
}
```

- O **void** antes da função **miau** significa que ela não retorna um valor e, da mesma forma, no geral , não podemos fazer nada com o resultado de **miau** , então apenas a chamamos.

A abstração aqui leva a um design melhor, já que agora temos a flexibilidade de reutilizar nossa função **miau** em vários lugares no futuro.

Vejamos outro exemplo de abstração, get_positive_int.c:

```
#include <cs50.h>
#include <stdio.h>

int get_positive_int(void);

int main(void)
{
     int i = get_positive_int();
     printf(“%i\n”);
}

// Solicita um número inteiro positivo ao usuário
int get_positive_int(void)
{
     int n;
     do
     {
          n = get_int(“Número positivo: \n”); 
	 }
     while(n < 1);
     return n;
}
```

- Temos nossa própria função que chama **get_int** repetidamente até que tenhamos algum número inteiro que não seja menor que 1. Com um loop do-while, nosso programa fará algo primeiro, depois verificará alguma condição e repetirá enquanto a condição for verdadeira. Um loop while, por outro lado, verificará a condição primeiro.
- Precisamos declarar nosso inteiro **n** fora do loop do-while, pois precisamos usá-lo após o término do loop. O **escopo** de uma variável em C se refere ao contexto, ou linhas de código, dentro do qual ela existe. Em muitos casos, serão as chaves ao redor da variável.
- Observe que a função **get_positive_int** agora começa com **int**, indicando que ela tem um valor de retorno do tipo **int** e, em principal, nós o armazenamos em **i** após chamar **get_positive_int()**. Em **get_positive_int**, temos uma nova palavra-chave, **return** , para retornar o valor **n** para onde quer que a função foi chamada.
