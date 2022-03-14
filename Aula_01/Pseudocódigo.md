## Pseudocódigo

Podemos escrever **pseudocódigo**, que é uma representação de nosso algoritmo em inglês preciso (ou alguma outra linguagem humana):
```
1 Pegue a lista telefônica
2 Abra no meio da lista telefônica
3 Olhe para a página
4 Se a pessoa estiver na página
5  Ligar para pessoa
6 Caso contrário, se a pessoa estiver mais para o início do livro
7  Abrir no meio da metade esquerda do livro
8  Volte para a linha 3
9 Caso contrário, se a pessoa estiver mais para o final do livro
10  Abrir no meio da metade direita do livro
11  Volte para a linha 3
12 Caso contrário
13  Desistir
```
- Com essas etapas, verificamos a página do meio, decidimos o que fazer e repetimos. Se a pessoa não estiver na página e não houver mais páginas sobrando no livro, paramos. E esse caso final é particularmente importante para lembrar. Quando outros programas em nossos computadores esquecem esse caso final, eles podem travar ou parar de responder, uma vez que encontraram um caso que não foi contabilizado, ou continuar a repetir o mesmo trabalho continuamente nos bastidores, sem fazer nenhum progresso.

Algumas dessas linhas começam com verbos ou ações. Começaremos chamando estas *funções*:
```
1 **Pegue** a lista telefônica
2 **Abra** no meio da lista telefônica
3 **Olhe** para a página
4 Se a pessoa estiver na página
5  **Ligar** para pessoa
6 Caso contrário, se a pessoa estiver mais para o início do livro
7  **Abrir** no meio da metade esquerda do livro
8  Volte para a linha 3
9 Caso contrário, se a pessoa estiver mais para o final do livro
10  **Abrir** no meio da metade direita do livro
11  Volte para a linha 3
12 Caso contrário
13  **Desistir**
```
Também temos ramificações que levam a caminhos diferentes, como bifurcações na estrada, que chamaremos de *condições*:
```
1 Pegue a lista telefônica
2 Abra no meio da lista telefônica
3 Olhe para a página
4 **Se** a pessoa estiver na página
5  Ligar para pessoa
6 **Caso contrário**, se a pessoa estiver mais para o início do livro
7  Abrir no meio da metade esquerda do livro
8  Volte para a linha 3
9 **Caso contrário**, se a pessoa estiver mais para o final do livro
10  Abrir no meio da metade direita do livro
11  Volte para a linha 3
12 **Caso contrário**
13  Desistir
```
E as perguntas que decidem para onde vamos são chamadas de *expressões booleanas* , que eventualmente resultam em um valor de sim ou não, verdadeiro ou falso:
```
1 Pegue a lista telefônica
2 Abra no meio da lista telefônica
3 Olhe para a página
4 Se **a pessoa estiver na página**
5  Ligar para pessoa
6 Caso contrário, se **a pessoa estiver mais para o início do livro**
7  Abrir no meio da metade esquerda do livro
8  Volte para a linha 3
9 Caso contrário, se **a pessoa estiver mais para o final do livro**
10  Abrir no meio da metade direita do livro
11  Volte para a linha 3
12 Caso contrário
13  Desistir
```
Por último, temos palavras que criam ciclos, onde podemos repetir partes de nosso programa, chamadas *loops*:

```

1 Pegue a lista telefônica
2 Abra no meio da lista telefônica
3 Olhe para a página
4 Se a pessoa estiver na página
5  Ligar para pessoa
6 Caso contrário, se a pessoa estiver mais para o início do livro
7  Abrir no meio da metade esquerda do livro
8  **Volte para a linha 3**
9 Caso contrário, se a pessoa estiver mais para o final do livro
10  Abrir no meio da metade direita do livro
11  **Volte para a linha 3**
12 Caso contrário
13  Desistir

```

