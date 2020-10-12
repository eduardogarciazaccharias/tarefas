# questao13
#include <stdio.h>
#include <stdlib.h>

int main()
{
    float *v, aux;
    int n;
    printf("Qual o tamanho do vetor que deseja: ");
    scanf("%d", &n);
    v = (float *)calloc(n,sizeof(float));
    for(int i = 0; i < n; i++){
        printf("Digite o elemento da posicao %d: ",i+1);
        scanf("%f", &v[i]);
    }

    for(int i = 0; i < n; i++){
        for(int j = 0; j < n; j++){
                if(v[i] < v[j]){
                    aux = v[i];
                    v[i] = v[j];
                    v[j] = aux;
                }

        }
    }

    for(int i = 0; i < n; i++){
        printf("%.1f  ", v[i]);
    }
    free(v);
    return 0;
}
