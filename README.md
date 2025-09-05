# super-trunfo-c
#include <stdio.h>

typedef struct {
    char nome[50];
    int ataque;
    int defesa;
    int velocidade;
} Carta;

int main() {
    Carta carta1 = {"Dragao", 80, 60, 40};
    Carta carta2 = {"Fenix", 70, 50, 90};

    int escolha;

    printf("Escolha o atributo para comparar:\n");
    printf("1 - Ataque\n2 - Defesa\n3 - Velocidade\n");
    scanf("%d", &escolha);

    switch(escolha) {
        case 1:
            if (carta1.ataque > carta2.ataque)
                printf("%s vence!\n", carta1.nome);
            else if (carta1.ataque < carta2.ataque)
                printf("%s vence!\n", carta2.nome);
            else
                printf("Empate!\n");
            break;
        case 2:
            if (carta1.defesa > carta2.defesa)
                printf("%s vence!\n", carta1.nome);
            else if (carta1.defesa < carta2.defesa)
                printf("%s vence!\n", carta2.nome);
            else
                printf("Empate!\n");
            break;
        case 3:
            if (carta1.velocidade > carta2.velocidade)
                printf("%s vence!\n", carta1.nome);
            else if (carta1.velocidade < carta2.velocidade)
                printf("%s vence!\n", carta2.nome);
            else
                printf("Empate!\n");
            break;
        default:
            printf("Opção inválida!\n");
    }

    return 0;
}
