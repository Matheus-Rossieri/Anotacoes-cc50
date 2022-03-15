## **Expressões booleanas, loops**

Podemos traduzir um bloco “para sempre” no Scratch com:

```
while (true)
{
    printf (“Oi mundo!\n”); 
}
```

- A palavra-chave **while** (enquanto) requer uma condição, então usamos **true** como a expressão booleana para garantir que nosso loop seja executado para sempre. **while** dirá ao computador para verificar se a expressão é avaliada como **true**(verdadeira) e, em seguida, executar as linhas dentro das chaves. Em seguida, ele repetirá isso até que a expressão não seja mais verdadeira. Nesse caso, **true** sempre será true, então nosso loop é um **loop infinito** ou que será executado para sempre.

Poderíamos fazer algo um certo número de vezes com **while**:

```
int i = 0;
while (i < 50)
{
    printf(“Oi mundo!\n”); 
    i++;
}
```

- Criamos uma variável,**i**, e a definimos como 0. Então, enquanto **i** é menor que 50, executamos algumas linhas de código, incluindo uma em que adicionamos 1 a **i** a cada passagem. Dessa forma, nosso loop acabará eventualmente, quando **i** atingir um valor de 50.
- Nesse caso, estamos usando a variável **i** como contador, mas como ela não tem nenhum propósito adicional, podemos simplesmente chamá-la de **i**.

Mesmo que possamos iniciar a contagem em 1, como demonstrado abaixo, por convenção devemos começar em 0:

```
int i = 1;
while (i <= 50)
{
     printf(“Oi mundo!\n”); 
     i++;
}
```

Outra solução correta, mas possivelmente menos bem projetada, pode comecar com o contador em 50 e contar para trás:

```
int i = 50;
while (i > 0)
{
     printf(“Oi mundo!\n”); 
     i--;
}
```

- Nesse caso, a lógica do nosso loop é mais difícil de raciocinar sem servir a nenhum propósito adicional e pode até mesmo confundir os leitores.

Finalmente, mais comumente, podemos usar a palavra-chave for:

```
int i = 0;
for (int i = 0; i < 50; i++)
{
    printf(“Oi mundo!\n”); 
}
```

- Novamente, primeiro criamos uma variável chamada **i** e a definimos como 0. Em seguida, verificamos que i < 50 toda vez que alcançamos o topo do loop, antes de executar qualquer código interno. Se essa expressão for verdadeira, executamos o código interno. Finalmente, depois de executar o código interno, usamos **i++** para adicionar um a i , e o loop se repete.
- O loop do tipo **for** é mais elegante do que o loop do tipo **while** nesse caso, uma vez que tudo relacionado ao loop está na mesma linha, e somente o código que realmente desejamos executar multiplas vezes está dentro do loop.

Observe que para muitas dessas linhas de código, como condições do tipo **if** e loops do tipo **for**, não colocamos um ponto e vírgula no final. É assim que a linguagem C foi projetada, muitos anos atrás, e uma regra geral é que apenas as linhas para ações ou verbos têm ponto e vírgula no final.
