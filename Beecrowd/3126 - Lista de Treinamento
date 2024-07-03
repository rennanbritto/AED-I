#include <stdio.h>

#define MAX_CANDIDATOS 1000

int main() {
    int C;
    int lista_candidatos[MAX_CANDIDATOS];

    // número de candidatos
    scanf("%d", &C);

    // Leitura dos candidatos que compareceram (1) ou não (0)
    for (int i = 0; i < C; ++i) {
        scanf("%d", &lista_candidatos[i]);
    }

    // Contagem dos candidatos que compareceram (valor 1)
    int soma = 0;
    for (int i = 0; i < C; ++i) {
        if (lista_candidatos[i] == 1) {
            soma++;
        }
    }

    // Impressão do resultado
    printf("%d\n", soma);

    return 0;
}
