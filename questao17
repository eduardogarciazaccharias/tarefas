# questao17

#include <stdio.h>
#include <stdlib.h>

void somaVetores(float a[], float b[], float c[], int d){
        for(int i = 0; i < d; i++){
            c[i] = a[i] + b[i];
        }
        for(int i = 0; i < d; i++){
        printf("%.1f  ", c[i]);    //impressão do vetor organizado
    }
}

int main()
{
   float *v1, *v2, *v3;
    int n;
    printf("Qual o tamanho do vetor que deseja: ");
    scanf("%d", &n);                                  //escolhe o tamanho do vetor
    v1 = (float *)calloc(n,sizeof(float));
    v2 = (float *)calloc(n,sizeof(float));
    v3 = (float *)calloc(n,sizeof(float));             //alocação de memoria
    for(int i = 0; i < n; i++){
        printf("Digite o elemento da posicao %d do vetor 1: ",i+1);   //digitando os valores do vetor 1
        scanf("%f", &v1[i]);
    }

    for(int i = 0; i < n; i++){
        printf("Digite o elemento da posicao %d do vetor 2: ",i+1);   //digitando os valores do vetor 2
        scanf("%f", &v2[i]);
    }

    somaVetores(v1, v2, v3, n);  //função realizando a soma e imprimindo no terminal
    free(v1);
    free(v2);
    free(v3);
    return 0;
}
