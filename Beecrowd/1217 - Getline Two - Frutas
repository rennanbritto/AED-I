#include <string.h>
#include <stdio.h>

int main() {
    char *posicao_espaco;
    int num_dias, quantidade_frutas;
    char linha[10000];
    double valor_total, total_peso_dia, total_gasto_dia;

    scanf("%d\n", &num_dias);

    total_peso_dia = 0.0;
    total_gasto_dia = 0.0;
    
    for(int dia = 1; dia <= num_dias; ++dia) {
        scanf("%lf\n", &valor_total);
        scanf("%[^\n]", linha);

        quantidade_frutas = 1;
        posicao_espaco = strchr(linha, ' ');
        while(posicao_espaco != NULL) {
            ++quantidade_frutas;
            posicao_espaco = strchr(posicao_espaco + 1, ' ');
        }

        printf("day %d: %d kg\n", dia, quantidade_frutas);

        total_peso_dia += quantidade_frutas;
        total_gasto_dia += valor_total;
    }

    total_peso_dia /= num_dias;
    total_gasto_dia /= num_dias;

    printf("%.2lf kg by day\nR$ %.2lf by day\n", total_peso_dia, total_gasto_dia);

    return 0;
}
