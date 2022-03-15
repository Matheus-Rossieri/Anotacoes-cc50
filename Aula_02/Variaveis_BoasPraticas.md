## **Variáveis e Açúcar Sintático(boas práticas)**

No Scratch, tínhamos blocos como “set [counter] to (0)” que definem uma variável para algum valor. Em C, escreveríamos `int contador = 0; `para o mesmo efeito.

Podemos aumentar o valor de uma variável com ` contador = contador + 1; ` , onde olhamos primeiro para o lado direito, pegando o valor original do contador , adicionando 1 e, em seguida, armazenando-o no lado esquerdo (de volta ao contador, neste caso).

C também suporta **açúcar sintático** ou expressões abreviadas para a mesma funcionalidade. Nesse caso, poderíamos dizer de maneira equivalente` contador += 1;` para adicionar um ao contador antes de armazená-lo novamente. Também poderíamos escrever `contador++;` , e podemos aprender isso (e outros exemplos) examinando a documentação ou outras referências online.
