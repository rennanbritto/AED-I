#include <stdio.h>

int main() {
  
    int porcoes[5] = {300, 1500, 600, 1000, 150};

    // Quantidades de porções que cada personagem vai comer
    int quantidades[5];
    int chica = 225;
    int total = 0;

    for (int i = 0; i < 5; i++) {
        scanf("%d", &quantidades[i]);
    }

    for (int i = 0; i < 5; i++) {
        total += porcoes[i] * quantidades[i];
    }

    total += chica;

    printf("%d\n", total);

    return 0;
}
