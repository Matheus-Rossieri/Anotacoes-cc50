## **Operadores, limitações, truncamento**

Existem vários operadores matemáticos que podemos usar também:

-  \+ para adição
-  \- para subtração
-  \* para multiplicação
-  / para divisão
-  % para calcular o resto

Faremos um novo programa, **additional.c**:

```
#include <cs50.h>
#include <stdio.h>

int main(void) 
{
     int x = get_int("x: ");
 
     int y = get_int("y: ");

     printf("%i\n", x + y); 
}
```

- Vamos incluir arquivos de cabeçalho para as bibliotecas que sabemos que iremos usar, e então vamos chamar get_int para obter inteiros do usuário, armazenando-os em variáveis nomeadas **x** e **y**.
- Em seguida, em **printf**, imprimiremos um espaço reservado para um inteiro, **%i** , seguido por uma nova linha. Ja que nós queremos imprimir a soma de **x** e **y**, vamos passar em **x + y** para **printf** para substituir na string.
- Vamos salvar, executar make add no terminal e depois ./addition para ver nosso programa funcionando. Se digitarmos algo que não seja um inteiro, veremos get_int nos pedindo um inteiro novamente. Se digitarmos um número muito grande, como **4000000000**, get_int nos alertará novamente. Isso ocorre porque, como em muitos sistemas de computador, um **int** no CS50 IDE é de 32 bits, que pode conter apenas cerca de quatro bilhões de valores diferentes. E uma vez que os inteiros podem ser positivos ou negativos, o maior valor positivo para um **int** só pode ser cerca de dois bilhões, com um valor negativo mais baixo de cerca de dois bilhões negativos, para um total de cerca de quatro bilhões de valores totais.

Podemos mudar nosso programa para usar o tipo **long**:

```
#include <cs50.h>
#include <stdio.h>

int main (void) 
{
     long x = get_long("x: ");
 
     long y = get_long("y: ");

     printf("%li\n", x + y); 
}
```

- Agora podemos digitar inteiros maiores e ver um resultado correto conforme o esperado.

Sempre que obtivermos um erro durante a compilação, é uma boa ideia rolar para cima para ver o primeiro erro e corrigi-lo primeiro, já que às vezes um erro no início do programa fará com que o resto do programa seja interpretado com erros também.

Vejamos outro exemplo, **truncation.c**:

```
#include <cs50.h>
#include <stdio.h>

int main (void) 
{
     // Pega os números do usuário
     int x = get_int("x: ");
     int y = get_int("y: ");
     
     // Divide x por y
     float z = x / y;
     printf("%li\n", x + y); 
}
```

- Vamos armazenar o resultado de **x** dividido por **y** em **z** , um valor de virgula flutuante ou número real, e imprimi-lo também como um valor flutuante.
- Mas quando compilamos e executamos nosso programa, vemos z impresso como números inteiros como **0,000000** ou **1,000000** . Acontece que, em nosso código, **x / y** é dividido como dois inteiros primeiro , portanto, o resultado fornecido pela operação de divisão também é um inteiro. O resultado é **truncado** , com o valor após a vírgula perdida. Mesmo que **z** seja um **float**, o valor que estamos armazenando nele já é um número inteiro.

Para corrigir isso, vamos fazer o ***casting\***, ou seja, converter nossos números inteiros para float antes de dividi-los:

```
float z = (float) x / (float) y;
```

O resultado será um float como esperamos e, na verdade, podemos lançar apenas um de **x** ou **y** e obter um float também.

 
