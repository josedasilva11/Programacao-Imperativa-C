

## Estrutura de um Programa em C

Um programa em C começa com a inclusão de bibliotecas necessárias e a definição da função `main`, que é o ponto de entrada do programa.

```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```

## Declaração de Variáveis

As variáveis são declaradas especificando o tipo e o nome da variável. Elas podem ser inicializadas no momento da declaração.

```c
int x;       // Declaração
int y = 10;  // Declaração e inicialização
int a, b, c; // Declaração múltipla

```

## Os principais tipos numéricos em C incluem:

### char
- Representa um caractere.
- Ocupa 1 byte de memória.
- Pode armazenar valores inteiros entre -128 e 127 (para signed char) ou entre 0 e 255 (para unsigned char).

```c
#include <stdio.h>

int main() {
    char c = 'A'; // Representa o caractere 'A'
    unsigned char uc = 255; // Máximo valor para unsigned char

    printf("Caractere: %c\n", c);
    printf("Valor unsigned char: %u\n", uc);
    return 0;
}
```

### short
- Inteiro curto.
- Ocupa pelo menos 2 bytes de memória.
- Pode armazenar valores entre -32,768 e 32,767 (para short) ou entre 0 e 65,535 (para unsigned short).

```c
#include <stdio.h>

int main() {
    short s = 32767; // Máximo valor para short
    unsigned short us = 65535; // Máximo valor para unsigned short

    printf("Valor short: %d\n", s);
    printf("Valor unsigned short: %u\n", us);
    return 0;
}

```


### int 

- Inteiro padrão.
- Ocupa pelo menos 2 bytes de memória, geralmente 4 bytes.
- Pode armazenar valores entre -2,147,483,648 e 2,147,483,647 (para int) ou entre 0 e 4,294,967,295 (para unsigned int).




```c
#include <stdio.h>

int main() {
    int i = 2147483647; // Máximo valor para int
    unsigned int ui = 4294967295; // Máximo valor para unsigned int

    printf("Valor int: %d\n", i);
    printf("Valor unsigned int: %u\n", ui);
    return 0;
}

```


### long 
- Inteiro longo.
- Ocupa pelo menos 4 bytes de memória.
- Pode armazenar valores entre -2,147,483,648 e 2,147,483,647 (para long) ou entre 0 e 4,294,967,295 (para unsigned long).



```c

#include <stdio.h>

int main() {
    long l = 2147483647; // Máximo valor para long
    unsigned long ul = 4294967295; // Máximo valor para unsigned long

    printf("Valor long: %ld\n", l);
    printf("Valor unsigned long: %lu\n", ul);
    return 0;
}
```

### float 

- Ponto flutuante de precisão simples.
- Ocupa 4 bytes de memória.
- Pode armazenar números com ponto flutuante entre aproximadamente 1.2E-38 e 3.4E+38.

```c
#include <stdio.h>

int main() {
    float f = 3.14f; // Valor de ponto flutuante

    printf("Valor float: %f\n", f);
    return 0;
}

```

### double 

- Ponto flutuante de precisão dupla.
- Ocupa 8 bytes de memória.
- Pode armazenar números com ponto flutuante entre aproximadamente 2.3E-308 e 1.7E+308.

```c
#include <stdio.h>

int main() {
    double d = 3.141592653589793; // Valor de ponto flutuante de precisão dupla

    printf("Valor double: %lf\n", d);
    return 0;
}

```

















## Funções

### Definição e Declaração

As funções são blocos de código que executam uma tarefa específica e podem ser reutilizadas. Uma função deve ser declarada antes de ser usada e definida com seu corpo de código.

#### Declaração
A declaração de uma função informa ao compilador sobre a função, seu nome, tipo de retorno e parâmetros.

```c
int soma(int a, int b); // Declaração
```

#### Definição
A definição de uma função inclui a implementação da função.

```c
int soma(int a, int b) { // Definição
    return a + b;
}

```


Exemplo completo:

```c

#include <stdio.h>

int soma(int a, int b); // Declaração

int soma(int a, int b) { // Definição
    return a + b;
}

int main() {
    int resultado = soma(3, 4);
    printf("Resultado: %d\n", resultado);
    return 0;
}
```

### Passagem de Argumentos
Em C, os argumentos podem ser passados por valor ou por referência (usando ponteiros).

#### Passagem por Valor
Os valores dos argumentos são copiados para os parâmetros da função.

```c
int soma(int a, int b) {
    return a + b;
}

```
#### Passagem por Referência
Os endereços dos argumentos são passados para a função, permitindo a modificação dos valores originais.

```c
void incrementa(int *a) {
    (*a)++;
}

int main() {
    int x = 5;
    incrementa(&x);
    printf("x incrementado: %d\n", x);
    return 0;
}

```

## Comandos vs. Expressões
### Comandos
Comandos são instruções que alteram o estado do programa. Exemplos incluem atribuições, chamadas de funções, laços e condicionais.
```c
int x = 5; // Comando de atribuição

```

### Expressões
Expressões são combinações de valores, variáveis e operadores que produzem um valor. Elas podem ser usadas dentro de comandos.

```c
int y = 3 + 4; // 3 + 4 é uma expressão
int z = x * y; // x * y é uma expressão

```


## Operadores Aritméticos

Os operadores aritméticos básicos em C são:

- + (adição)
- - (subtração)
- * (multiplicação)
- / (divisão)
- % (módulo)

```c

int a = 10, b = 3;
int soma = a + b;      // Soma: 13
int subtracao = a - b; // Subtração: 7
int produto = a * b;   // Produto: 30
int quociente = a / b; // Quociente: 3
int resto = a % b;
```

### Outros Operadores
Além dos operadores aritméticos básicos, C possui outros operadores importantes:

#### Operadores Relacionais
Usados para comparar valores.

- == (igual a)
- != (diferente de)
- > (maior que)
- < (menor que)
- >= (maior ou igual a)
- <= (menor ou igual a)

```c
int a = 10, b = 5;
int resultado;

resultado = (a == b);  // Falso (0)
resultado = (a != b);  // Verdadeiro (1)
resultado = (a > b);   // Verdadeiro (1)
resultado = (a < b);   // Falso (0)
resultado = (a >= b);  // Verdadeiro (1)
resultado = (a <= b);  // Falso (0)

```
#### Operadores Lógicos

Usados para combinar expressões booleanas.

- && (E lógico)
- || (OU lógico)
- ! (NÃO lógico)

```c
int a = 1, b = 0;
int resultado;

resultado = (a && b); // Falso (0)
resultado = (a || b); // Verdadeiro (1)
resultado = !a;       // Falso (0)

```
#### Operadores de Atribuição
Usados para atribuir valores a variáveis.

- = (atribuição)
- += (adição e atribuição)
- -= (subtração e atribuição)
- *= (multiplicação e atribuição)
- /= (divisão e atribuição)
- %= (módulo e atribuição)

```c
int a = 10;
a += 5; // a agora é 15
a -= 3; // a agora é 12
a *= 2; // a agora é 24
a /= 4; // a agora é 6
a %= 3; // a agora é 0

```

#### Operadores Bitwise
Usados para operações em nível de bits.

- & (E bit a bit)
- | (OU bit a bit)
- ^ (OU exclusivo bit a bit)
- ~ (NÃO bit a bit)
- << (deslocamento à esquerda)
- >> (deslocamento à direita)

```c
int a = 5;    // 0101 em binário
int b = 3;    // 0011 em binário
int resultado;

resultado = a & b;  // 0001 (1 em decimal)
resultado = a | b;  // 0111 (7 em decimal)
resultado = a ^ b;  // 0110 (6 em decimal)
resultado = ~a;     // 1010 (em binário, -6 em decimal para sistemas de 4 bits)
resultado = a << 1; // 1010 (10 em decimal)
resultado = a >> 1; // 0010 (2 em decimal)

```

































































## Estruturas de Controle
### Condicionais
As estruturas condicionais são usadas para tomar decisões baseadas em condições. As principais são if, else if, else e switch.

if, else if, else
Estas estruturas permitem executar blocos de código diferentes com base em uma condição booleana.

```c
#include <stdio.h>

int main() {
    int a = 5;
    int b = 3;

    if (a > b) {
        printf("a é maior que b\n");
    } else if (a < b) {
        printf("a é menor que b\n");
    } else {
        printf("a é igual a b\n");
    }

    return 0;
}
```

### switch
O switch é usado para selecionar uma entre várias opções baseadas no valor de uma variável.

```c
#include <stdio.h>

int main() {
    int opcao = 2;

    switch(opcao) {
        case 1:
            printf("Opção 1 selecionada\n");
            break;
        case 2:
            printf("Opção 2 selecionada\n");
            break;
        case 3:
            printf("Opção 3 selecionada\n");
            break;
        default:
            printf("Opção inválida\n");
            break;
    }

    return 0;
}


```
## Laços de Repetição
Os laços de repetição são usados para executar um bloco de código várias vezes. As principais estruturas são for, while e do-while.

### for
O laço for é usado quando o número de iterações é conhecido.


```c

#include <stdio.h>

int main() {
    for (int i = 0; i < 10; i++) {
        printf("i = %d\n", i);
    }

    return 0;
}

```

### while
O laço while é usado quando a condição de término é verificada no início de cada iteração.

```c

#include <stdio.h>

int main() {
    int i = 0;

    while (i < 10) {
        printf("i = %d\n", i);
        i++;
    }

    return 0;
}

```

### do-while
O laço do-while é semelhante ao while, mas a condição de término é verificada no final de cada iteração, garantindo que o bloco de código seja executado pelo menos uma vez.
```c
#include <stdio.h>

int main() {
    int i = 0;

    do {
        printf("i = %d\n", i);
        i++;
    } while (i < 10);

    return 0;
}


```

## Entrada e Saída
### printf
A função printf é usada para imprimir saída formatada para a tela.

```c
#include <stdio.h>

int main() {
    int x = 10;
    float y = 3.14;
    char c = 'A';

    printf("Inteiro: %d\n", x);
    printf("Float: %.2f\n", y);
    printf("Caractere: %c\n", c);

    return 0;
}


```
### scanf
A função scanf é usada para ler a entrada do usuário.

```c
#include <stdio.h>

int main() {
    int x;
    float y;
    char c;

    printf("Digite um número inteiro: ");
    scanf("%d", &x);
    printf("Digite um número float: ");
    scanf("%f", &y);
    printf("Digite um caractere: ");
    scanf(" %c", &c); // Note o espaço antes de %c para ignorar caracteres em branco

    printf("Você digitou: %d, %.2f, %c\n", x, y, c);

    return 0;
}


```

### Códigos de Formatação
Os códigos de formatação em printf e scanf são usados para especificar o tipo de dados a serem lidos ou escritos.

- %d ou %i: Inteiro decimal.
- %f: Ponto flutuante.
- %c: Caractere.
- %s: String.
- %x: Inteiro hexadecimal.
- %o: Inteiro octal.
- %e ou %E: Notação científica.
- %%: Imprime um caractere '%'.

```c
#include <stdio.h>

int main() {
    int idade;
    float altura;
    char nome[50];

    printf("Digite seu nome: ");
    scanf("%s", nome);  // Não precisa do & para strings
    printf("Digite sua idade: ");
    scanf("%d", &idade);
    printf("Digite sua altura (em metros): ");
    scanf("%f", &altura);

    printf("Nome: %s\n", nome);
    printf("Idade: %d anos\n", idade);
    printf("Altura: %.2f metros\n", altura);

    return 0;
}


```































## Estruturas de Dados

### Arrays
Arrays são coleções de elementos do mesmo tipo armazenados em posições contíguas de memória. O acesso aos elementos é feito através de índices.

Declaração e Inicialização
```c
#include <stdio.h>

int main() {
    int arr[5] = {1, 2, 3, 4, 5}; // Declaração e inicialização
    for (int i = 0; i < 5; i++) {
        printf("Elemento %d: %d\n", i, arr[i]);
    }
    return 0;
}


```
### Strings
Strings são arrays de caracteres terminados com o caractere nulo (\0). Eles são usados para manipular texto.

Declaração e Inicialização

```c
#include <stdio.h>

int main() {
    char str[6] = "hello"; // Inclui o caractere nulo automaticamente
    printf("String: %s\n", str);
    return 0;
}


```
### Structs
Structs (estruturas) são usadas para agrupar variáveis de tipos diferentes em uma única unidade.

Declaração e Inicialização

```c
#include <stdio.h>

struct Ponto {
    float x;
    float y;
};

int main() {
    struct Ponto p1 = {0.0, 0.0}; // Declaração e inicialização
    printf("Ponto: (%.2f, %.2f)\n", p1.x, p1.y);
    return 0;
}


```

Acesso e Modificação dos Membros

```c
#include <stdio.h>

struct Ponto {
    float x;
    float y;
};

int main() {
    struct Ponto p1;
    p1.x = 1.0;
    p1.y = 2.0;
    printf("Ponto: (%.2f, %.2f)\n", p1.x, p1.y);
    return 0;
}


```





## Manipulação de Memória

### Apontadores
Apontadores são variáveis que armazenam endereços de memória. Eles são usados para manipular dados de forma eficiente.

Declaração e Inicialização

```c
#include <stdio.h>

int main() {
    int x = 10;
    int *p = &x; // p é um apontador para x
    printf("Valor de x: %d\n", x);
    printf("Endereço de x: %p\n", (void*)&x);
    printf("Valor de p (endereço de x): %p\n", (void*)p);
    printf("Valor apontado por p: %d\n", *p);
    
    *p = 20; // altera o valor de x para 20
    printf("Novo valor de x: %d\n", x);
    return 0;
}

```
## Alocação Dinâmica de Memória
A alocação dinâmica permite reservar memória em tempo de execução, usando as funções malloc, calloc e realloc, e liberar a memória com free.

### malloc
Aloca um bloco contínuo de memória.

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int *arr = (int *)malloc(5 * sizeof(int)); // aloca memória para 5 inteiros
    if (arr == NULL) {
        printf("Erro na alocação de memória\n");
        return 1;
    }

    for (int i = 0; i < 5; i++) {
        arr[i] = i * 2;
        printf("Elemento %d: %d\n", i, arr[i]);
    }

    free(arr); // libera a memória
    return 0;
}
```
### calloc
Aloca memória para um array de elementos e inicializa todos os bytes para zero.

```c

#include <stdio.h>
#include <stdlib.h>

int main() {
    int *arr = (int *)calloc(5, sizeof(int)); // aloca e inicializa memória para 5 inteiros
    if (arr == NULL) {
        printf("Erro na alocação de memória\n");
        return 1;
    }

    for (int i = 0; i < 5; i++) {
        printf("Elemento %d: %d\n", i, arr[i]);
    }

    free(arr); // libera a memória
    return 0;
}

```
### realloc
Redimensiona um bloco de memória previamente alocado.

```c

#include <stdio.h>
#include <stdlib.h>

int main() {
    int *arr = (int *)malloc(5 * sizeof(int)); // aloca memória para 5 inteiros
    if (arr == NULL) {
        printf("Erro na alocação de memória\n");
        return 1;
    }

    for (int i = 0; i < 5; i++) {
        arr[i] = i * 2;
        printf("Elemento %d: %d\n", i, arr[i]);
    }

    arr = (int *)realloc(arr, 10 * sizeof(int)); // redimensiona para 10 inteiros
    if (arr == NULL) {
        printf("Erro na realocação de memória\n");
        return 1;
    }

    for (int i = 5; i < 10; i++) {
        arr[i] = i * 2;
        printf("Elemento %d: %d\n", i, arr[i]);
    }

    free(arr); // libera a memória
    return 0;
}

```


















## Recursividade

A recursividade é uma técnica onde uma função se chama a si mesma para resolver subproblemas menores de um problema maior. Essa abordagem é particularmente útil em problemas que podem ser decompostos em casos menores do mesmo problema.

### Exemplo: Fatorial
O cálculo do fatorial de um número n é um exemplo clássico de recursão. O fatorial de n (denotado como n!) é o produto de todos os números inteiros positivos até n.

```c
#include <stdio.h>

// Função recursiva para calcular o fatorial
int fatorial(int n) {
    if (n == 0) return 1; // Caso base: fatorial de 0 é 1
    else return n * fatorial(n - 1); // Chamada recursiva
}

int main() {
    int num = 5;
    printf("Fatorial de %d é %d\n", num, fatorial(num));
    return 0;
}

```
Explicação
- Caso Base: O fatorial de 0 é definido como 1.
- Chamada Recursiva: Para n > 0, o fatorial de n é n multiplicado pelo fatorial de n - 1.

## Ordenação e Pesquisa

A ordenação por inserção é um algoritmo simples e eficiente para ordenar pequenas listas de elementos. Funciona da mesma forma que as pessoas ordenam cartas num jogo: começa com uma carta na mão e, a cada nova carta, insere-a na posição correta em relação às que já estão ordenadas.

### Ordenação por Inserção
```c
#include <stdio.h>

// Função para ordenar um array usando ordenação por inserção
void insertionSort(int arr[], int n) {
    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;

        // Move os elementos do array que são maiores que a chave
        // para uma posição à frente da sua posição atual
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}

// Função para imprimir um array
void printArray(int arr[], int n) {
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
}

int main() {
    int arr[] = {12, 11, 13, 5, 6};
    int n = sizeof(arr)/sizeof(arr[0]);

    insertionSort(arr, n);
    printArray(arr, n);

    return 0;
}

```
Explicação
- Iteração: O algoritmo percorre o array começando do segundo elemento.
- Inserção: Cada elemento é comparado com os anteriores e inserido na posição correta.



### Pesquisa Binária
A pesquisa binária é um algoritmo eficiente para encontrar um elemento em um array ordenado. Funciona dividindo repetidamente o array ao meio até encontrar o elemento buscado ou determinar que ele não está no array.

```c

#include <stdio.h>

// Função para realizar a pesquisa binária em um array ordenado
int binarySearch(int arr[], int l, int r, int x) {
    while (l <= r) {
        int m = l + (r - l) / 2;

        // Verifica se x está presente no meio
        if (arr[m] == x) return m;

        // Se x for maior, ignore a metade esquerda
        if (arr[m] < x) l = m + 1;

        // Se x for menor, ignore a metade direita
        else r = m - 1;
    }

    // Se não estiver presente no array
    return -1;
}

// Função para imprimir o resultado da pesquisa
void printResult(int index) {
    if (index != -1) {
        printf("Elemento encontrado no índice %d\n", index);
    } else {
        printf("Elemento não encontrado\n");
    }
}

int main() {
    int arr[] = {2, 3, 4, 10, 40};
    int n = sizeof(arr)/sizeof(arr[0]);
    int x = 10;
    
    int result = binarySearch(arr, 0, n - 1, x);
    printResult(result);

    x = 5;
    result = binarySearch(arr, 0, n - 1, x);
    printResult(result);

    return 0;
}

```

Explicação
- Divisão e Conquista: O array é dividido ao meio.
- Comparação: O elemento central é comparado com o elemento buscado.
- Redução do Espaço de Busca: Se o elemento central não é o buscado, o algoritmo continua a busca na metade relevante do array.


