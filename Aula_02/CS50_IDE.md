## CS50 IDE

Para começar a escrever nosso código rapidamente, usaremos uma ferramenta para o curso, o [**CS50 IDE**](https://ead.napratica.org.br/enrollments/6753432/courses/84414/course_contents/”https://ide.cs50.io/”) , um ambiente de desenvolvimento integrado que inclui programas e recursos para escrever código. CS50 IDE é construído sobre um IDE baseado em nuvem muito popular, usado por programadores gerais, mas com recursos educacionais adicionais e personalização.

Abriremos o IDE e, após o login, veremos uma tela como esta:

![IDE do CC50](https://edools-3-production.s3.amazonaws.com/org-6988%2Fschool-7227%2F068639d0bceb54f6ef253e32984ed242%2Fcs50_ide.png)

- O painel superior, em branco, conterá arquivos de texto nos quais podemos escrever nosso código.
- O painel inferior, uma janela de **terminal**, nos permitirá digitar vários comandos e executá-los, incluindo programas do nosso código acima.

Nosso IDE é executado na nuvem e vem com um conjunto padrão de ferramentas, mas saiba que também existem muitos IDEs baseados em desktop, oferecendo mais personalização e controle para diferentes propósitos de programação, ao custo de maior tempo e esforço para configurá-los.

No IDE, iremos para Arquivo> Novo arquivo e, em seguida, Arquivo> Salvar para salvar nosso arquivo como **hello.c** , indicando que nosso arquivo será um código escrito em C. Veremos que o nome de nossa guia de fato mudou para **hello.c** , e agora vamos colar o código que vimos acima:

```
#include <stdio.h>
int main(void)
{
    printf("olá, mundo"); 
}
```

Para executar nosso programa, usaremos uma **CLI**, ou **interface de linha de comando** , um *prompt* (um “gatilho”, por assim dizer) ao qual respondemos inserindo comandos de texto. Isso contrasta com a **interface gráfica do usuário**, ou GUI, como o Scratch, onde temos imagens, ícones e botões além do texto.
