#include <stdio.h>

// Função para ordenar um array em ordem decrescente
void ordenar_notas(int notas[], int n) {
    int i, j;
    for (i = 0; i < n - 1; i++) {
        for (j = 0; j < n - i - 1; j++) {
            if (notas[j] < notas[j + 1]) {
                // Troca usando XOR
                notas[j] ^= notas[j + 1];
                notas[j + 1] ^= notas[j];
                notas[j] ^= notas[j + 1];
            }
        }
    }
}

int main() {
    int casos;
    scanf("%d", &casos);

    for (int caso = 0; caso < casos; caso++) {
        int alunos;
        scanf("%d", &alunos);

        int notas[alunos];
        for (int i = 0; i < alunos; i++) {
            scanf("%d", &notas[i]);
        }

        // Copiar notas para um array auxiliar para comparar mudanças
        int notas_original[alunos];
        for (int i = 0; i < alunos; i++) {
            notas_original[i] = notas[i];
        }

        ordenar_notas(notas, alunos);

        // Contar quantos alunos não mudaram de posição
        int nao_mudaram = 0;
        for (int i = 0; i < alunos; i++) {
            if (notas[i] == notas_original[i]) {
                nao_mudaram++;
            }
        }
        printf("%d\n", nao_mudaram);
    }

    return 0;
}
