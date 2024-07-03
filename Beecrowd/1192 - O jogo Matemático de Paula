#include <stdio.h>

int main() {
    int N;
    scanf("%d", &N); 
    
    while (N--) {
        char seq[4]; // Array para armazenar os três caracteres
        scanf("%s", seq); 
        char digito1 = seq[0];
        char letra = seq[1];
        char digito2 = seq[2];
        
        int num1 = digito1 - '0'; // Converte char para inteiro (dígito1)
        int num2 = digito2 - '0';
        
        int resultado;
        
        if (letra >= 'A' && letra <= 'Z') { 
            resultado = num2 - num1;
        } else if (letra >= 'a' && letra <= 'z') { 
            resultado = num1 + num2;
        } else {
            continue;
        }
        
        if (num1 == num2) {
            resultado = num1 * num2;
        }
        
        printf("%d\n", resultado);
    }
    
    return 0;
}
