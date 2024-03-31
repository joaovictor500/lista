# lista
Questao 01 
Vamos analisar cada expressão e determinar o valor de acordo com as definições dadas:

p == &i;

Esta expressão verifica se o valor armazenado em p é igual ao endereço de i.
O valor de p é o endereço de i, portanto, esta expressão é verdadeira.
Resultado: Verdadeiro (1).
*p - *q;

Aqui, *p é o valor apontado por p, que é o valor de i, e *q é o valor apontado por q, que é o valor de j.
Então, *p - *q é 3 - 5, que resulta em -2.
Resultado: -2.
**&p;

&p obtém o endereço de p, que é o endereço do ponteiro p.
* desreferencia esse endereço, o que significa que estamos acessando o valor apontado por p, que é o endereço de i.
** desreferencia novamente para acessar o valor apontado por esse endereço, que é o valor de i.
Resultado: 3.
3 - *p/(*q) + 7;

Primeiro, *p é o valor de i, que é 3.
Em seguida, (*q) é o valor de j, que é 5.
Portanto, 3 - *p/(*q) + 7 é 3 - 3/5 + 7.
Considerando a precedência dos operadores, a divisão é realizada primeiro: 3/5 resulta em 0 (a parte fracionária é descartada em operações entre inteiros).
Então, a expressão se torna 3 - 0 + 7, que é 10.
Resultado: 10.
Portanto, os valores das expressões são:

p == &i;: Verdadeiro (1).
*p - *q;: -2.
**&p;: 3.
3 - *p/(*q) + 7;: 10.

Quetao 02 \ 





Questao 03 \ p = &i;

Esta expressão é legal, pois está atribuindo o endereço da variável inteira i ao ponteiro p.
*q = &j;

Esta expressão é ilegal. Aqui, você está tentando atribuir o endereço da variável j a um inteiro (*q). Isso é inválido porque *q é um inteiro, e você não pode atribuir um endereço a um inteiro diretamente.
p = &*&i;

Esta expressão é legal. &i obtém o endereço de i, * desreferencia esse endereço, e & obtém o endereço resultante, que é novamente atribuído a p.
i = (*&)j;

Esta expressão é ilegal. (*&) não é uma operação válida. Isso tenta desreferenciar o endereço de j, mas não é uma sintaxe válida em C.
i = *&j;

Esta expressão é legal. *&j é basicamente redundante. * desreferencia o endereço de j, e então i recebe o valor resultante.
i = *&*&j;

Esta expressão é legal. É semelhante à anterior, *&*& é redundante e apenas obtém o valor de j e atribui a i.
q = *p;

Esta expressão é ilegal. Aqui, você está tentando atribuir o valor apontado por p a q, mas q é um ponteiro e *p é um inteiro. Atribuir um inteiro a um ponteiro diretamente não é permitido sem uma conversão explícita.
i = (*p)++ + *q;

Esta expressão é legal. (*p)++ incrementa o valor apontado por p e retorna o valor original, que é adicionado ao valor apontado por q e atribuído a i.







Questao 05 \  contador/valor/valor/endereco/endereco
i= vet[0] 1 1.1 *(f x 0) = 1.1 &vet[0] = 6644B60 (f +
0)=66F44B60
i= 1 vet[1] 2.2 *(f + 1) = 2.2 Svet[1] = 66F44B64 (f+
1) = 66F44B64
i = 2 vet[2] 3.3 *(f+2) =3:3 &vet[2] 6644B68 (f +
2) =66F44B68
i = 3 vet[3] = 4.4 *(f + 3) = 4.4 &vet[3] = 66F44B6C (f +
3)= 66F44B6C
L = 4 vet[4] = 5.5 *(f + 4) = 5.5 &vet[4] 66F44B70 (f+
4) = 66F44B70

Questao 06 \ Para determinar qual expressão referencia o valor do terceiro elemento do vetor pulo[], devemos entender como a aritmética de ponteiros funciona em C.

Supondo que pulo[] seja um vetor do tipo int, o acesso ao terceiro elemento do vetor pode ser feito de várias maneiras. Vamos analisar cada expressão:

*(pulo + 2);

Esta expressão adiciona 2 ao ponteiro pulo, o que resulta no endereço do terceiro elemento do vetor, e então desreferencia esse endereço para acessar o valor armazenado.
Portanto, esta expressão referencia o valor do terceiro elemento do vetor.
*(pulo + 4);

Esta expressão adiciona 4 ao ponteiro pulo, o que resulta no endereço do quinto elemento do vetor, e então desreferencia esse endereço para acessar o valor armazenado.
Portanto, esta expressão referencia o valor do quinto elemento do vetor.
pulo + 4;

Esta expressão adiciona 4 ao ponteiro pulo, resultando no endereço do quinto elemento do vetor.
Esta expressão não desreferencia o ponteiro para acessar o valor armazenado. Ela simplesmente retorna o endereço do quinto elemento do vetor.
pulo + 2;

Esta expressão adiciona 2 ao ponteiro pulo, resultando no endereço do terceiro elemento do vetor.
Similarmente à expressão anterior, esta expressão não desreferencia o ponteiro para acessar o valor armazenado. Ela simplesmente retorna o endereço do terceiro elemento do vetor.
Portanto, apenas as expressões 1 e 3 referenciam o valor do terceiro elemento do vetor:

*(pulo + 2);
pulo + 2;

Questao 07 \ 
Vamos analisar cada expressão:

p = mat + 1;

Esta expressão é válida. mat é um ponteiro para o primeiro elemento do array mat, e ao somar 1, estamos avançando para o próximo elemento do array. Portanto, p aponta para o segundo elemento do array.
p = mat;

Esta expressão também é válida. mat é um ponteiro para o primeiro elemento do array mat, então atribuir mat a p simplesmente faz com que p aponte para o primeiro elemento do array.
p = mat;

Essa expressão parece ser uma duplicata da anterior. Provavelmente foi um erro de digitação ao colocar duas vezes a mesma expressão. A segunda ocorrência de p = mat; não adiciona nada de novo e não afeta a validade da expressão.
x = (*mat);

Esta expressão também é válida. (*mat) dereferencia o ponteiro mat, acessando o valor do primeiro elemento do array. Esse valor é então atribuído à variável x.
Portanto, todas as expressões fornecidas são válidas em termos de sintaxe e semântica em C.

Questao 08 \ 
Esse programa em C imprime os elementos do array vet[] na saída padrão. Vamos analisar o que cada parte do código faz:

int vet[] = {4, 9, 13};: Declara e inicializa um array de inteiros chamado vet com os valores {4, 9, 13}. O tamanho do array é determinado automaticamente pelo número de elementos na lista de inicialização.

int i;: Declara uma variável inteira i para ser usada como contador no loop.

for(i=0;i<3;i++){: Inicia um loop for com a variável i inicializada em 0. O loop continuará enquanto i for menor que 3 (o tamanho do array vet[]). Em cada iteração, i é incrementada.

printf("%d ", *(vet+i));: Dentro do loop, esta linha imprime o valor do elemento atual do array vet[]. *(vet+i) é uma maneira de acessar o valor do elemento no índice i do array vet[]. O operador * é usado para desreferenciar o ponteiro resultante de vet+i, o que significa que estamos acessando o valor armazenado na posição de memória apontada por vet+i. O %d na função printf() é um especificador de formato para imprimir um valor inteiro. O espaço " " após %d é apenas para separar os valores impressos na saída.

}: Fecha o loop for.

No geral, este programa imprime os elementos do array vet[] (que são 4, 9 e 13) na saída padrão, separados por um espaço. O resultado seria:

Copy code
4 9 13

Questao 09 #include <stdio.h>

struct teste {
    int x;
    char nome[10]; // Deixei um tamanho arbitrário para o nome
};

int main() {
    struct teste *s;

    // Alocando memória para a struct
    s = (struct teste *)malloc(sizeof(struct teste));

    // Atribuindo valores aos membros da struct
    s->x = 3;
    strcpy(s->nome, "jose");

    // Imprimindo os valores
    printf("%d\n", s->x);
    printf("%s\n", s->nome);

    // Liberando a memória alocada
    free(s);

    return 0;
    3
    jose

    Questao 10 \ Declaração de ponteiro constante para int: Na linha int const *x = 3;, você está tentando declarar um ponteiro constante para um inteiro, mas está inicializando-o com o valor inteiro 3. Isso resultará em um warning de conversão de tipos e um comportamento indefinido.

Operação inválida: Na linha printf("%d", ++(*x));, você está tentando incrementar o valor para o qual x aponta (*x), mas x foi declarado como um ponteiro constante. Tentar modificar o valor apontado por um ponteiro constante resultará em comportamento indefinido.

Como resultado, a saída do programa não é previsível. Dependendo da implementação e das otimizações do compilador, pode resultar em uma falha de segmentação, um valor incorreto impresso ou até mesmo executar sem problemas. No entanto, é importante notar que este programa não é um código C válido e deve ser corrigido para funcionar corretamente.




