#include <stdio.h>

// Função para contar o número de trocas necessárias para ordenar o vetor usando ordenação por inserção
int contarTrocas(int *vetor, int tamanho) {
    int trocas = 0;

    for (int i = 1; i < tamanho; ++i) {
        int chave = vetor[i];
        int j = i - 1;

        // Move elementos do vetor que são maiores que a chave para uma posição à frente
        while (j >= 0 && vetor[j] > chave) {
            vetor[j + 1] = vetor[j];
            --j;
            ++trocas;
        }
        vetor[j + 1] = chave;
    }

    return trocas;
}

int main() {
    int numCasos, tamanhoVetor;
    int vagao[50];

    scanf("%d", &numCasos);

    for (int i = 0; i < numCasos; ++i) {
        scanf("%d", &tamanhoVetor);

        for (int j = 0; j < tamanhoVetor; ++j) {
            scanf("%d", &vagao[j]);
        }

        int trocas = contarTrocas(vagao, tamanhoVetor);
        printf("Optimal train swapping takes %d swaps.\n", trocas);
    }

    return 0;
}
