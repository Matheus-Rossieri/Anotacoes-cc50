## **Ferramentas**

Com toda a nova sintaxe, é fácil cometer erros ou esquecer algo. Temos algumas ferramentas criadas pela equipe para nos ajudar.

Podemos esquecer de incluir uma linha de código e, quando tentamos compilar nosso programa, vemos muitas linhas de mensagens de erro que são difíceis de entender, pois o compilador pode ter sido projetado para um público mais técnico. **help50** é um comando que podemos executar para explicar problemas em nosso código de uma forma mais amigável. Podemos executá-lo adicionando help50 à frente de um comando que estamos tentando, como help50 make hello , para obter conselhos que possam ser mais compreensíveis.

Acontece que, em C, novas linhas e indentação geralmente não afetam a forma como nosso código é executado. Por exemplo, podemos alterar nossa **função principal(main)** para uma linha, `int main (void) {printf ("hello, world");},` mas é muito mais difícil de ler, então consideramos que tem um estilo ruim. Podemos executar style50 , como style50 hello.c, com o nome do arquivo de nosso código-fonte, para ver sugestões de novas linhas e recuo.

Além disso, podemos adicionar **comentários** , notas em nosso código-fonte para nós mesmos ou para outras pessoas que não afetem a forma como nosso código é executado. Por exemplo, podemos adicionar uma linha como `// Cumprimentar o usuário`, com duas barras // para indicar que a linha é um comentário e, em seguida, escrever o propósito do nosso código ou programa para nos ajudar a lembrar mais tarde.

**check50** irá verificar a exatidão do nosso código com alguns testes automatizados. A equipe escreve testes especificamente para alguns dos programas que escreveremos no curso, e as instruções para usar o check50 serão incluídas em cada conjunto de problemas ou laboratório, conforme necessário. Depois de executar check50, veremos algum output nos informando se nosso código passou nos testes relevantes.

O IDE CS50 também nos dá o equivalente a nosso próprio computador na nuvem, em algum lugar da internet, com nossos próprios arquivos e pastas. Se clicarmos no ícone da pasta no canto superior esquerdo, veremos uma árvore de arquivos, uma GUI dos arquivos em nosso IDE:

![Árvore de arquivos do IDE CS50](https://edools-3-production.s3.amazonaws.com/org-6988%2Fschool-7227%2Fb085df9e7be60154f15c034c899eadb7%2Fcs50_ide_file_tree.png)

- Para abrir um arquivo, podemos apenas clicar duas vezes nele. hello.c é o código-fonte que acabamos de escrever, e hello em si terá muitos pontos vermelhos, cada um dos quais são caracteres não imprimíveis, pois representam instruções binárias para nossos computadores.

 
