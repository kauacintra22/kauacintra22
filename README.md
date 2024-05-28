#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int inteiro;
    float pontoFlutuante;
    char caractere;

    
    printf("digite uma string");
    fgets(str, sizeof(str), stdin);
    
    str[strcspn(str, "\n")] = 0;

    printf("digite um número inteiro");
    scanf("%d", &inteiro);

    
    printf("digite um número de ponto flutuante");
    scanf("%f", &pontoFlutuante);

    while (getchar() != '\n');

    
    printf("digite um caracter");
    scanf("%c", &caractere);
    
    int strLength = strlen(str);
    int intSquared = inteiro * inteiro; 
    float halfFloat = pontoFlutuante / 2.0;
    char nextChar = caractere + 1; 

    
    printf("\nResultados das manipulações:\n");
    printf("String: %s (tamanho: %d)\n", str, strLength);
    printf("Número inteiro: %d (quadrado: %d)\n", inteiro, intSquared);
    printf("Número de ponto flutuante: %.2f (metade: %.2f)\n", pontoFlutuante, halfFloat);
    printf("Caractere: %c (próximo caractere: %c)\n", caractere, nextChar);

    return 0;
}
