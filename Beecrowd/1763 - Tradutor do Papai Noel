#include <stdio.h>
#include <string.h>

// Estrutura para armazenar os dados de cada país
typedef struct {
    char pais[30];
    char frase[50];
} PaisFrase;

int main() {
    // Lista de países e suas respectivas frases
    PaisFrase bancoDeDados[] = {
        {"brasil", "Feliz Natal!"},
        {"alemanha", "Frohliche Weihnachten!"},
        {"austria", "Frohe Weihnacht!"},
        {"coreia", "Chuk Sung Tan!"},
        {"espanha", "Feliz Navidad!"},
        {"grecia", "Kala Christougena!"},
        {"estados-unidos", "Merry Christmas!"},
        {"inglaterra", "Merry Christmas!"},
        {"australia", "Merry Christmas!"},
        {"portugal", "Feliz Natal!"},
        {"suecia", "God Jul!"},
        {"turquia", "Mutlu Noeller"},
        {"argentina", "Feliz Navidad!"},
        {"chile", "Feliz Navidad!"},
        {"mexico", "Feliz Navidad!"},
        {"antardida", "Merry Christmas!"},
        {"canada", "Merry Christmas!"},
        {"irlanda", "Nollaig Shona Dhuit!"},
        {"belgica", "Zalig Kerstfeest!"},
        {"italia", "Buon Natale!"},
        {"libia", "Buon Natale!"},
        {"siria", "Milad Mubarak!"},
        {"marrocos", "Milad Mubarak!"},
        {"japao", "Merii Kurisumasu!"}
    };
    
    int n = sizeof(bancoDeDados) / sizeof(bancoDeDados[0]); // Número de países no banco de dados
    
    char paisConsulta[30];
    while (scanf("%s", paisConsulta) != EOF) { // Ler os países da entrada até o final do arquivo
        int encontrado = 0;
        for (int i = 0; i < n; i++) {
            if (strcmp(paisConsulta, bancoDeDados[i].pais) == 0) {
                printf("%s\n", bancoDeDados[i].frase);
                encontrado = 1;
                break;
            }
        }
        if (!encontrado) {
            printf("--- NOT FOUND ---\n");
        }
    }

    return 0;
}
