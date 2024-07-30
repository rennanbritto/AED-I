#include <stdio.h>
#include <string.h>

// Função para deslocar caracteres maiúsculos e minúsculos 3 posições para a direita
void deslocar_direita(char* s) {
    for (int i = 0; s[i] != '\0'; i++) {
        if ((s[i] >= 'a' && s[i] <= 'z') || (s[i] >= 'A' && s[i] <= 'Z')) {
            s[i] += 3;
        }
    }
}

void inverter_string(char* s) {
    int n = strlen(s);
    for (int i = 0; i < n / 2; i++) {
        char temp = s[i];
        s[i] = s[n - i - 1];
        s[n - i - 1] = temp;
    }
}

void deslocar_esquerda(char* s) {
    int n = strlen(s);
    for (int i = n / 2; i < n; i++) {
        s[i] -= 1;
    }
}

int main() {
    int N;
    scanf("%d", &N);
    getchar();  // Consumir a nova linha após o número de casos

    char linha[1001];

    for (int i = 0; i < N; i++) {
        fgets(linha, sizeof(linha), stdin);
        linha[strcspn(linha, "\n")] = '\0';

        // Primeira fase
        deslocar_direita(linha);

        // Segunda
        inverter_string(linha);

        // Terceira
        deslocar_esquerda(linha);

        // Resultad final
        printf("%s\n", linha);
    }

    return 0;
}
