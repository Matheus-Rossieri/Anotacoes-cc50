## **Memória, imprecisão e estouro**

Nosso computador tem memória, em chips de hardware chamados RAM, memória de acesso aleatório. Nossos programas usam essa RAM para armazenar dados enquanto estão em execução, mas essa memória é finita.

Com **imprecision.c** , podemos ver o que acontece quando usamos valores flutuantes:

```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    float x = get_float("x: ");
    float y = get_float("y: ");
    	
    printf(“%.50f\n", x / y;); 
}
```

- Com **% .50f** , podemos especificar o número de casas decimais exibidas.
- Hmm, agora nós temos ...

x: 1
y: 10
0,10000000149011611938476562500000000000000000000000

- Acontece que isso é chamado de **imprecisão de vírgula flutuante**, em que não temos bits suficientes para armazenar todos os valores possíveis. Com um número finito de bits para um **float** , não podemos representar todos os números reais possíveis (dos quais existe um número *infinito* de), então o computador tem que armazenar o valor mais próximo que puder. E isso pode levar a problemas em que mesmo pequenas diferenças no valor se somam, a menos que o programador use alguma outra maneira para representar os valores decimais com a precisão necessária.

Na semana passada, quando tínhamos três bits e precisávamos contar mais do que sete (ou 111), adicionamos outro bit para obter oito, 1000 . Mas se tivéssemos apenas três bits disponíveis, não teríamos lugar para o 1 extra . Ele desapareceria e estaríamos de volta a 000. Esse problema é chamado de **overflow (“vazamento”) de inteiro**, pois um inteiro só pode atingir um tamanho especifico antes de ficar sem bits.

O problema Y2K surgiu porque muitos programas armazenavam o ano civil com apenas dois dígitos, como 98 para 1998 e 99 para 1999. Mas quando o ano 2000 se aproximou, os programas tiveram que armazenar apenas 00, levando a confusão entre os anos 1900 e 2000 .

Em 2038, também ficaremos sem bits para rastrear o tempo, já que há muitos anos alguns humanos decidiram usar 32 bits como o número padrão de bits para contar o número de segundos desde 1º de janeiro de 1970. Mas com 32 bits representando apenas números positivos, só podemos contar até cerca de quatro bilhões e, em 2038, atingiremos esse limite, a menos que atualizemos o software em todos os nossos sistemas de computador.
