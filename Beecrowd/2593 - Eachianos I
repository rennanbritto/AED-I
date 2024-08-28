#include <stdio.h>
#include <string.h>

#define TAMANHO_MAXIMO_TEXTO 10001
#define MAXIMO_PALAVRAS 128
#define TAMANHO_MAXIMO_PALAVRA 51

int main() {
    char texto[TAMANHO_MAXIMO_TEXTO];
    int n, i;
    char palavras[MAXIMO_PALAVRAS][TAMANHO_MAXIMO_PALAVRA];

    // Texto
    scanf("%10000[^\n]", texto);
    
    // Número de palavras
    scanf("%d", &n);

    // `Palavras de busca
    for (i = 0; i < n; i++) {
        scanf("%s", palavras[i]);
    }

    // Encontrar as posições das palavras no texto
    for (i = 0; i < n; i++) {
        char *pos = texto;
        int encontrou = 0;

        // Buscar a palavra no texto
        while ((pos = strstr(pos, palavras[i])) != NULL) {
            // Verificar se é isolada
            int inicio_palavra = (pos == texto) || (*(pos - 1) == ' ');
            int fim_palavra = (*(pos + strlen(palavras[i])) == ' ' || *(pos + strlen(palavras[i])) == '\0');

            if (inicio_palavra && fim_palavra) {
                if (encontrou) {
                    printf(" ");
                }
                printf("%ld", pos - texto);
                encontrou = 1;
            }
            pos++;
        }

        if (!encontrou) {
            printf("-1");
        }
        printf("\n");
    }

    return 0;
}
}
