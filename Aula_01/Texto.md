## Texto

Para representar as letras, tudo o que precisamos fazer é decidir como os números são mapeados para as letras. Alguns humanos, muitos anos atrás, decidiram coletivamente um mapeamento padrão de números em letras. A letra “A”, por exemplo, é o número 65, e “B” é 66 e assim por diante. Ao usar o contexto, como quando estamos olhando uma planilha ou um e-mail, diferentes programas podem interpretar e exibir os mesmos bits como números ou texto.

O mapeamento padrão, [ASCII](https://pt.wikipedia.org/wiki/ASCII), também inclui letras minúsculas e pontuação.

Se recebêssemos uma mensagem de texto com um padrão de bits que tivesse os valores decimais **72 , 73 e 33**, esses bits seriam mapeados para as letras **HI!**. Cada letra é normalmente representada com um padrão de oito bits, ou um **byte**, então as sequências de bits que receberíamos são **01001000 , 01001001 e 00100001.**

- Podemos já estar familiarizados com o uso de bytes como uma unidade de medida para dados, como em megabytes ou gigabytes, para milhões ou bilhões de bytes.

Com oito bits, ou um byte, podemos ter 28 ou 256 valores diferentes (incluindo zero). (O valor mais alto que podemos contar seria 255.)

Outros caracteres, como letras com acentos e símbolos em outros idiomas, fazem parte de um padrão chamado [Unicode](https://ead.napratica.org.br/enrollments/6753432/courses/84414/course_contents/”https://pt.wikipedia.org/wiki/Unicode”), que usa mais bits do que ASCII para acomodar todos esses caracteres.

- Quando recebemos um emoji, nosso computador está apenas recebendo um número binário que mapeia para a imagem do emoji baseado no padrão Unicode. Por exemplo, o emoji “rosto com lágrimas de alegria” tem apenas os bits **000000011111011000000010**:

  ![](https://edools-3-production.s3.amazonaws.com/org-6988%2Fschool-7227%2F512657e41deb7c4ee12bc597ef039e78%2Fface_with_tears_of_joy.png)
