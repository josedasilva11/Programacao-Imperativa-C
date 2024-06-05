

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

- Condicionais: if, else if, else, switch.
- Laços de Repetição: for, while, do-while.

```c
if (a > b) {
    // código se a maior que b
} else {
    // código se a menor ou igual a b
}

for (int i = 0; i < 10; i++) {
    // comandos
}
```

## Entrada e Saída

As funções padrão para I/O incluem printf para saída e scanf para entrada.

```c
#include <stdio.h>

int main() {
    int x;
    printf("Digite um número: ");
    scanf("%d", &x);
    printf("Você digitou: %d\n", x);
    return 0;
}


```

## Estruturas de Dados

- Arrays: Colecção de elementos do mesmo tipo.
- Strings: Arrays de caracteres terminados com \0.
- Structs: Agrupamento de variáveis de tipos diferentes.

```c
int arr[5] = {1, 2, 3, 4, 5};
char str[6] = "hello";

struct Ponto {
    float x;
    float y;
};

struct Ponto p1 = {0.0, 0.0};

```

## Manipulação de Memória

- Apontadores: Variáveis que armazenam endereços de memória.
- Alocação Dinâmica: Uso de malloc, calloc, realloc, free.

```c
int x = 10;
int *p = &x;
*p = 20; // altera o valor de x para 20

int *arr = (int *)malloc(5 * sizeof(int));
if (arr == NULL) {
    // erro na alocação
}
free(arr); // libera a memória
```


## Recursividade

Funções que chamam a si mesmas, como no cálculo do fatorial.

```c
int fatorial(int n) {
    if (n == 0) return 1;
    else return n * fatorial(n - 1);
}

```

## Ordenação e Pesquisa

Algoritmos clássicos de ordenação e pesquisa, como a ordenação por inserção e a pesquisa binária.
```c
void insertionSort(int arr[], int n) {
    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}

int binarySearch(int arr[], int l, int r, int x) {
    while (l <= r) {
        int m = l + (r - l) / 2;
        if (arr[m] == x) return m;
        if (arr[m] < x) l = m + 1;
        else r = m - 1;
    }
    return -1;
}
```





