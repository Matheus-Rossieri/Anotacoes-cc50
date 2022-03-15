## **Comandos**

Como o IDE CS50 é um computador virtual na nuvem, também podemos executar comandos disponíveis no Linux, um sistema operacional como o macOS ou Windows.

No terminal, podemos digitar **ls**, abreviação de list, para ver uma lista de arquivos e pastas na pasta atual:

```
~ / $ ls
ola* ola.c
```

- **ola** está em verde com um asterisco para indicar que podemos executá-lo como um programa.

Também podemos remover arquivos com **rm** , com um comando como rm ola. Isso nos solicitará uma confirmação e podemos responder com **y** ou **n** para sim ou não.

Com **mv** , ou **move** , podemos renomear arquivos. Com mv hello.c goodbye.c , renomeamos nosso arquivo ola.c com o nome goodbye.c.

Com **mkdir** , ou *diretório make*, podemos criar pastas ou diretórios. Se executarmos mkdir lecture, veremos uma pasta chamada lecture e podemos mover arquivos para diretórios com um comando como mv ola.c lecture/.

Para *mudar os diretórios* em nosso terminal, podemos usar **cd** , como em cd lecture /. Nosso prompt mudará de ~/ para ~/ lecture /, indicando que estamos no diretório de palestras(lecture) dentro de ~ . ~ representa nosso diretório inicial ou a pasta padrão de nível superior de nossa conta.

Também podemos usar .. como uma abreviação para a “pasta-mae”, ou a pasta que contém aquela na qual estamos . Dentro de ~ / lecture / , podemos executar mv ola.c .. para movê-lo de volta para ~ , já que é a pasta-mae de lecture / . cd .. , da mesma forma, mudará o diretório do nosso terminal para a mae atual. Um único ponto ,. , refere-se ao diretório atual, como em ./ola.

Agora que nossa pasta lecture/ está vazia, podemos removê-la com rmdir lecture/ também.
