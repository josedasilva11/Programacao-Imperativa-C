

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


## Funções

As funções em C são definidas para modularizar o código. Uma função deve ser declarada e definida com seus parâmetros e tipo de retorno.

```c
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
## Comandos vs. Expressões

- Comandos: Alteram o estado do programa (e.g., atribuição).
- Expressões: Denotam valores e podem ser usadas em comandos.

```c
int x = 5; // Comando
int y = 3 + 4; // Expressão

```

## Operadores Aritméticos

Os operadores básicos incluem +, -, *, /, %.

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





