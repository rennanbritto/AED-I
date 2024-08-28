#include <stdio.h>
#include <stdlib.h>

// Estrutura que representa uma aresta no grafo, com dois vértices (roteadores) e o peso (custo do cabo)
typedef struct {
    int vertice1, vertice2, peso;
} Aresta;

// Função para encontrar o representante de um conjunto (utilizada para evitar ciclos)
int encontrar(int pai[], int i) {
    if (pai[i] == i)
        return i;
    return encontrar(pai, pai[i]);
}

// Função para unir dois conjuntos diferentes
void unirConjuntos(int pai[], int rank[], int x, int y) {
    int raizX = encontrar(pai, x);
    int raizY = encontrar(pai, y);

    if (rank[raizX] < rank[raizY]) {
        pai[raizX] = raizY;
    } else if (rank[raizX] > rank[raizY]) {
        pai[raizY] = raizX;
    } else {
        pai[raizY] = raizX;
        rank[raizX]++;
    }
}

// Função de comparação usada para ordenar as arestas pelo peso (custo do cabo)
int comparar(const void *a, const void *b) {
    return ((Aresta*)a)->peso - ((Aresta*)b)->peso;
}

int main() {
    int numRoteadores, numCabos;
    scanf("%d %d", &numRoteadores, &numCabos);

    Aresta arestas[numCabos];
    for (int i = 0; i < numCabos; i++) {
        scanf("%d %d %d", &arestas[i].vertice1, &arestas[i].vertice2, &arestas[i].peso);
    }

    // Ordena as arestas pelo peso em ordem crescente
    qsort(arestas, numCabos, sizeof(Aresta), comparar);

    // Arrays para armazenar o pai de cada conjunto e a altura (rank) de cada conjunto
    int pai[numRoteadores+1];
    int rank[numRoteadores+1];
    for (int i = 1; i <= numRoteadores; i++) {
        pai[i] = i;
        rank[i] = 0;
    }

    int custoTotal = 0;
    int arestasNaAGM = 0;

    // Algoritmo de Kruskal para encontrar a Árvore Geradora Mínima (AGM)
    for (int i = 0; i < numCabos && arestasNaAGM < numRoteadores - 1; i++) {
        int vertice1 = arestas[i].vertice1;
        int vertice2 = arestas[i].vertice2;
        int peso = arestas[i].peso;

        // Verifica se a adição dessa aresta criará um ciclo
        if (encontrar(pai, vertice1) != encontrar(pai, vertice2)) {
            unirConjuntos(pai, rank, vertice1, vertice2);
            custoTotal += peso;
            arestasNaAGM++;
        }
    }

    // Imprime o custo total da nova infraestrutura de rede
    printf("%d\n", custoTotal);

    return 0;
}
