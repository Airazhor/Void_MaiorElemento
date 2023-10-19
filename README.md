Atividade

Desenvolva uma função que receba como parâmetro um array de inteiros contendo N valores. Esta função pretende identificar o maior elemento presente no array e determinar quantas vezes esse elemento ocorre. Por exemplo, considerando um array com os seguintes elementos: 5, 2, 15, 3, 7, 15, 8, 6, 15, a função deve retornar para o programa que a chamou o valor 15 e o número 3 (indicando que o número 15 aparece 3 vezes no array). É importante destacar que esta função deve ser do tipo void, ou seja, não retorna nenhum valor diretamente ao programa principal.



#include<stdio.h>
#include <stdlib.h>

int vmaximo, repet; //Utilizo variáveis globais para armazenar o valor máximo e a contagem de repetições

void AcharMaiorE(int elementos[], int num_elementos) {
    int j;
    
    vmaximo = elementos[0]; // Inicia o valor máximo com o primeiro elemento

    for (j = 0; j < num_elementos; j++) {
        if (vmaximo <= elementos[j])
            vmaximo = elementos[j]; //Atualiza o valor máximo se um elemento maior for encontrado
        }
    }

    for (j = 0; j < num_elementos; j++) {
     if (vmaximo == elementos[j]) {
         repet++; // Conta quantas vezes o valor máximo ocorre no array
         }
    }
}
int main() {
    int N;
    int i = 0;
    
    printf("Olá, Que quantidade de números tera sua lista?:\n");
    scanf ("%d", &N);

    int lista[N];

    for (i = 0; i < N; i++) {
        printf("\nEntre com o número %d:\n", i + 1);
        scanf ("%d", &lista[i]);
    }
    AcharMaiorE(lista, N); // Chama a função que vai encontrar o valor máximo e a contar quantas vezes se repete 

    printf("\nO elemento de maior valor é: %d\n", vmaximo);
    printf("Este número se repetiu %d vez(es)\n", repet);

    return 0; 
    }
