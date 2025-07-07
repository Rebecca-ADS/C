#include <stdio.h>

// Funções matemáticas
float soma(float x, float y) {
    return x + y;
}

float subtracao(float x, float y) {
    return x - y;
}

float multiplicacao(float x, float y) {
    return x * y;
}

float divisao(float x, float y) {
    return x / y;
}

// Função principal
int main() {
    int opcao;
    float a, b, resultado;

    do {
        printf("\n=== CALCULADORA EM C ===\n");
        printf("1. Soma\n");
        printf("2. Subtração\n");
        printf("3. Multiplicação\n");
        printf("4. Divisão\n");
        printf("0. Sair\n");
        printf("Escolha uma opção: ");
        scanf("%d", &opcao);

        if (opcao >= 1 && opcao <= 4) {
            printf("Digite o primeiro número: ");
            scanf("%f", &a);
            printf("Digite o segundo número: ");
            scanf("%f", &b);
        }

        switch(opcao) {
            case 1:
                resultado = soma(a, b);
                printf("Resultado: %.2f\n", resultado);
                break;
            case 2:
                resultado = subtracao(a, b);
                printf("Resultado: %.2f\n", resultado);
                break;
            case 3:
                resultado = multiplicacao(a, b);
                printf("Resultado: %.2f\n", resultado);
                break;
            case 4:
                if (b != 0) {
                    resultado = divisao(a, b);
                    printf("Resultado: %.2f\n", resultado);
                } else {
                    printf("Erro: divisão por zero!\n");
                }
                break;
            case 0:
                printf("Saindo da calculadora...\n");
                break;
            default:
                printf("Opção inválida!\n");
        }

    } while(opcao != 0);

    return 0;
}
