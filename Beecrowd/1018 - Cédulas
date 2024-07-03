#include <stdio.h>

int main() {
    int valor;
    scanf("%d", &valor);
    
    printf("%d\n", valor);
    
    // o número de cada nota
    int notas100 = valor / 100;
    valor = valor % 100; // calcula o resto, para ir à proxima linha
    int notas50 = valor / 50;
    valor = valor % 50;
    int notas20 = valor / 20;
    valor = valor % 20;
    int notas10 = valor / 10;
    valor = valor % 10;
    int notas5 = valor / 5;
    valor = valor % 5;
    int notas2 = valor / 2;
    valor = valor % 2;
    int notas1 = valor;
    
    printf("%d nota(s) de R$ 100,00\n", notas100);
    printf("%d nota(s) de R$ 50,00\n", notas50);
    printf("%d nota(s) de R$ 20,00\n", notas20);
    printf("%d nota(s) de R$ 10,00\n", notas10);
    printf("%d nota(s) de R$ 5,00\n", notas5);
    printf("%d nota(s) de R$ 2,00\n", notas2);
    printf("%d nota(s) de R$ 1,00\n", notas1);
    
    return 0;
}
