#include <stdio.h>
#include <string.h>

#define MAX_LEN 1001
#define TAM_ALFAB 26

int main() {
    char sequencia[MAX_LEN];
    
    while (scanf("%s", sequencia) != EOF) {
        // Vetor para armazenar a frequência de cada letra
        int frequencia[TAM_ALFAB] = {0};
        
        // Contagem da frequência de cada letra
        for (int i = 0; i < strlen(sequencia); i++) {
            frequencia[sequencia[i] - 'a']++;
        }
        
        // Contagem das letras com frequência ímpar
        int letras_impares = 0;
        for (int i = 0; i < TAM_ALFAB; i++) {
            if (frequencia[i] % 2 != 0) {
                letras_impares++;
            }
        }
        
        // Número mínimo de letras a serem adicionadas
        int letras_adicionais = letras_impares > 0 ? letras_impares - 1 : 0;
        
        printf("%d\n", letras_adicionais);
    }
    
    return 0;
}
