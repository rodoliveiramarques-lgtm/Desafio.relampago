# Gabarito Completo: Desafio Relâmpago de Programação em C

# 1. Imprimir os números de 1 a 10
A estrutura `for` é a escolha ideal quando conhecemos previamente os limites inicial e final da repetição.

#include <stdio.h>

int main() {
    int i;
    
    for (i = 1; i <= 10; i++) {
        printf("%d\n", i);
    }
    
    return 0;
}


# 2. Imprimir os números de 10 a 1 (Ordem Decrescente)
Utiliza a mesma lógica do desafio anterior, alterando o valor inicial para `10`, a condição de parada para maior ou igual a `1` e aplicando o operador de decremento (`i--`).

#include <stdio.h>

int main() {
    int i;
    
    for (i = 10; i >= 1; i--) {
        printf("%d\n", i);
    }
    
    return 0;
}




#3. Soma dos números de 1 a 100
Usa uma variável acumuladora (`soma`) inicializada estritamente em `0`. A cada repetição do laço, o valor atual de `i` é adicionado a ela.


#include <stdio.h>

int main() {
    int i;
    int soma = 0;
    
    for (i = 1; i <= 100; i++) {
        soma = soma + i;
    }
    
    printf("A soma de 1 a 100 eh: %d\n", soma);
    
    return 0;
}



# 4. Imprimir de 1 até N
Solicita a entrada de um número limite `N` via `scanf`. O laço `for` incrementa o contador enquanto `i` for menor ou igual a `N`.


#include <stdio.h>

int main() {
    int N, i;
    
    printf("Digite um numero inteiro: ");
    scanf("%d", &N);
    
    for (i = 1; i <= N; i++) {
        printf("%d\n", i);
    }
    
    return 0;
}




# 5. Contar a quantidade de dígitos de um número
A estrutura `do-while` é ideal aqui porque precisamos executar a verificação pelo menos uma vez (o que garante que o número `0` seja contabilizado como 1 dígito). A lógica consiste em remover a última casa decimal dividindo o número sucessivamente por `10` até que ele se torne zero.


#include <stdio.h>

int main() {
    int numero, contador = 0;
    
    printf("Digite um numero inteiro: ");
    scanf("%d", &numero);
    
    // Converte números negativos para positivos para ignorar o sinal 
    if (numero < 0) {
        numero = -numero;
    }
    
    do {
        contador++;
        numero = numero / 10;
    } while (numero > 0);
    
    printf("O numero possui %d digitos.\n", contador);
    
    return 0;
}
