#include <stdio.h>
#include <stdlib.h>

int main() {
    int ingressocomum = 0;
    int ingressomeia = 0;
  int ingressoespe = 0;
    int totalingresso = 0;
    float precomum = 40.0;
    float precomeia = 20.0;
  float precoespe = 0.0;

  printf("\n******** Bem vindo ao CineArte Museu ********\n");
  
  printf("\nSistema de Compra de Ingressos\n");

    while (1) {
        printf("\nMenu:\n");
        printf("\n1. Ingresso Inteira - R$%.2f\n",precomum);
        printf("2. Ingresso Meia - R$%.2f\n", precomeia);
      printf("3. Ingresso Especial - R$%.2f\n", precoespe);
        printf("4. Concluir compra\n");

        int choice;
        printf("\nEscolha uma opcao de ingresso para compra e em seguida, a opcao CONCLUIR COMPRA: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("\nQuantos ingressos comuns voce deseja comprar? ");
                scanf("%d", &ingressocomum);
                break;
          
            case 2:
                printf("\nQuantos ingressos meia voce deseja comprar? ");
                scanf("%d", &ingressomeia);
                break;
          
            case 3: 
                printf("\nQuantos ingressos especiais voce deseja comprar?");
          break;
          
          case 4:
                totalingresso = ingressocomum + ingressomeia + ingressoespe;
                
      if (totalingresso > 0) {
      float precototal = (ingressocomum * precomum) + (ingressomeia * precomeia) + (ingressoespe * precoespe);
            
    printf("\nResumo da compra:\n");
        
    printf("Ingressos comuns: %d\n", ingressocomum);
    printf("Ingressos meia: %d\n", ingressomeia);
    printf ("Ingressos especiais: %d\n", ingressoespe);
        
    printf("\n Total de Ingressos: %d\n", totalingresso);
    
    printf("\n Total a pagar: R$%.2f\n", precototal);
                } else {
                    printf("Nenhum ingresso foi selecionado.\n");
                }
                return 0;
            default:
                printf("Opção inválida. Tente novamente.\n");
        }
    }

    return 0;
}
