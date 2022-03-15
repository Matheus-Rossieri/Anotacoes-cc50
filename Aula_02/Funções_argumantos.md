## **Funções e argumentos**

Usaremos as mesmas ideias que exploramos no Scratch.

**Funções** são pequenas ações ou verbos que podemos usar em nosso programa para fazer algo, e as entradas para funções são chamadas de **argumentos.**

- Por exemplo, o bloco “say” (“dizer”) no Scratch pode ter considerado algo como “olá, mundo” como um argumento. Em C, a função de imprimir algo na tela é chamada de **printf**(com **f** significando texto “formatado”, que veremos em breve). E em C, passamos os argumentos entre parênteses, como em `**printf ("hello, world")**`; . As aspas duplas indicam que queremos imprimir as letras **hello, world** literalmente, e o ponto-e-vírgula no final indica o fim de nossa linha de código.

As funções também podem ter dois tipos de saídas:

- **efeitos colaterais**, como algo impresso na tela,

- e

   

  valores de retorno

  , um valor que é passado de volta ao nosso programa que podemos usar ou armazenar para mais tarde.

  - O bloco “ask” (“perguntar”) no Scratch, por exemplo, criou um bloco “answer” (“responder”).

Para obter a mesma funcionalidade do bloco “ask”, usaremos uma **biblioteca** ou um conjunto de código já escrito. A Biblioteca CS50 incluirá algumas funções básicas e simples que podemos usar imediatamente. Por exemplo, **get_string** pedirá ao usuário uma string, ou alguma sequência de texto, e a retornará ao nosso programa. **get_string** recebe algum input e o usa como prompt para o usuário, como **“Qual é o seu nome?”**, e nós teremos que salvá-lo em uma variável com:

```
string answer = get_string("Qual é o seu nome?");
```

- Em C, o “**=**” indica **atribuição** ou configuração do valor à direita para a variável à esquerda. E o programa chamará a função get_string primeiro para então obter seu output.
- E também precisamos indicar que nossa variável chamada answer é do **tipo** string, então nosso programa saberá interpretar os zeros e uns como texto.
- Finalmente, precisamos nos lembrar de adicionar um ponto-e-vírgula para encerrar nossa linha de código.

No Scratch, também usamos o bloco “answer” dentro de nossos blocos “join” (“juntar”) e “say”. Em C, faremos isso:

```
printf("olá,% s", resposta);
```

- O %s é chamado de **código de formatação**, o que significa apenas que queremos que a função printf substitua uma variável onde está o marcador %s. E a variável que queremos usar é answer, que passamos para printf como outro argumento, separado do primeiro por uma vírgula. `(printf ("hello, answer"))` iria literalmente imprimir hello, answer sempre.)

De volta ao IDE CS50, nós implementaremos o que descobrimos:

```
#include <cs50.h>
#include <stdio.h>
int main(void)
{
     string answer = get_string("Qual é o seu nome?");
     printf("olá, %s", resposta);
}
```

- Precisamos dizer ao compilador para incluir a Biblioteca CS50, com **`#include <cs50.h>`,** para que possamos usar a função **get_string.**
- Também temos a oportunidade de escrever o código usando um “estilo” que favoreca intuitividade, já que poderíamos nomear nossa variável de resposta com qualquer coisa, mas um nome mais descritivo nos ajudará a entender sua finalidade melhor do que um nome mais curto como a ou x.

Depois de salvar o arquivo, precisaremos recompilar nosso programa com make hello, já que alteramos apenas o código-fonte, mas não o código de máquina compilado. Outras linguagens ou IDEs podem não exigir que recompilemos manualmente nosso código depois de alterá-lo, mas aqui temos a oportunidade de ter mais controle e compreensão do que está acontecendo nos bastidores.

Agora, ./hello executará nosso programa e solicitará nosso nome conforme pretendido. Podemos notar que o próximo prompt é impresso imediatamente após a saída de nosso programa, como em hello, Brian ~ / $ . Podemos adicionar uma nova linha após a saída de nosso programa, de modo que o próximo prompt esteja em sua própria linha, com \n:

```
printf("olá, %s\n" ,resposta);
```

\n é um exemplo de **sequência de escape** ou algum texto que na verdade representa algum outro texto.
