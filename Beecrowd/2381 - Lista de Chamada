#include <stdio.h>
#include <string.h>

#define MIN_N 1
#define MAX_N 100
#define MAX_NAME_LENGTH 21

// Função para ordenar os nomes em ordem alfabética
void ordenarNomes(char nomes[MAX_N][MAX_NAME_LENGTH], int n) {
    int i, j;
    char temp[MAX_NAME_LENGTH];

    for (i = 0; i < n - 1; i++) {
        for (j = 0; j < n - i - 1; j++) {
            if (strcmp(nomes[j], nomes[j + 1]) > 0) {
                strcpy(temp, nomes[j]);
                strcpy(nomes[j], nomes[j + 1]);
                strcpy(nomes[j + 1], temp);
            }
        }
    }
}

int main() {
    int N, K;
    char nome[MAX_N][MAX_NAME_LENGTH];

    // Entrada do número de alunos e o número sorteado
    scanf("%d %d", &N, &K);

    // Verificação dos limites de N e K
    if (N < MIN_N || N > MAX_N || K < MIN_N || K > N) {
        printf("Erro: Valores de N e/ou K fora do intervalo permitido.\n");
        return 1;
    }

    // Entrada dos nomes dos alunos
    for (int i = 0; i < N; i++) {
        scanf("%s", nome[i]);
        // Verificação do tamanho dos nomes
        if (strlen(nome[i]) < 1 || strlen(nome[i]) > 20) {
            printf("Erro: Tamanho do nome fora do intervalo permitido.\n");
            return 1;
        }
    }

    // Ordenar os nomes em ordem alfabética
    ordenarNomes(nome, N);

    // O aluno sorteado é o K-ésimo aluno na lista de chamada
    printf("%s\n", nome[K - 1]);

    return 0;
}
