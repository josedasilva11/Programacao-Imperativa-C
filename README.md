# Programacao-Imperativa-C

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

- 'char': Representa um caractere.
- 'short': Inteiro curto.
- 'int': Inteiro padrão.
- 'long': Inteiro longo.
- 'float': Ponto flutuante de precisão simples.
- 'double': Ponto flutuante de precisão dupla.

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

















































