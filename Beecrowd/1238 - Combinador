#include <stdio.h>
#include <string.h>

void combinar_strings(const char* s1, const char* s2, char* resultado) {
    int len1 = strlen(s1); // Comprimento da primeira string
    int len2 = strlen(s2); // Comprimento da segunda string
    int i = 0, j = 0, k = 0;

    // Alterna as letras das duas strings
    while (i < len1 && j < len2) {
        resultado[k++] = s1[i++]; // Adiciona um caractere de s1
        resultado[k++] = s2[j++]; // Adiciona um caractere de s2
    }

    // Adiciona os caracteres restantes de s1 (se houver, em caso de uma ser mais longa que a outra)
    while (i < len1) {
        resultado[k++] = s1[i++];
    }

    // Adiciona os caracteres restantes de s2 (se houver, como acima)
    while (j < len2) {
        resultado[k++] = s2[j++];
    }

    // Termina a string resultante com o caractere nulo
    resultado[k] = '\0';
}

int main() {
    int N; 
    scanf("%d", &N);
    getchar(); // Consome a nova linha após o número de casos

    char s1[51], s2[51], resultado[102];

    for (int i = 0; i < N; i++) {
        scanf("%s %s", s1, s2);

        combinar_strings(s1, s2, resultado);
      
        printf("%s\n", resultado);
    }

    return 0;
}
