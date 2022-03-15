## Compilação

No terminal no painel inferior de nosso IDE, iremos **compilar** nosso código antes de podermos executá-lo. Os computadores só entendem binário, que também é usado para representar instruções como imprimir algo na tela. Nosso **código-fonte** foi escrito em caracteres que podemos ler, mas precisa ser compilado: convertido em **código de máquina**, padrões de zeros e uns que nosso computador possa entender diretamente.

Um programa chamado **compilador** pegará o código-fonte como entrada e produzirá o código de máquina como saída. No IDE CS50, já temos acesso a um compilador, por meio de um comando chamado **make** . Em nosso terminal, digitaremos make hello, que encontrará automaticamente nosso arquivo hello.c com nosso código-fonte e o compilará em um programa chamado hello. Haverá alguma saída, mas nenhuma mensagem de erro em amarelo ou vermelho, então nosso programa foi compilado com sucesso.

Para executar nosso programa, digitaremos outro comando, ./hello, que procura na pasta atual , . , para um programa chamado hello e o executa.
