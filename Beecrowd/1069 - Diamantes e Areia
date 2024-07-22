#include <stdio.h>
#include <string.h>

int conta_diamantes(const char *str) {
    int abre_chaves = 0;  // Conta o número de <
    int diamantes_completos = 0; 

    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] == '<') {
            abre_chaves++;  // Incrementa ao encontrar um <
        } else if (str[i] == '>' && abre_chaves > 0) {
            diamantes_completos++;  // Encontra um diamante
            abre_chaves--;  // Diminui a contagem de < disponíveis
        }
    }

    return diamantes_completos;
}

int main() {
    int N;
    
    scanf("%d", &N); 

    char P[N][100]; 
    int resultado[N]; 

    for (int i = 0; i < N; i++) {
        scanf("%s", P[i]); 
        resultado[i] = conta_diamantes(P[i]);  // Conta diamantes para cada string
    }
    
    for (int i = 0; i < N; i++) {
        printf("%d\n", resultado[i]);
    }
    
    return 0;
}
