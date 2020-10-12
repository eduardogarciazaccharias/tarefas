# questao14

#include <stdio.h>
#include <stdlib.h>

int comparaCrescente(const void * a,const void * b){  //função que faz parte da qsort, comparando dois valores
    if(*(float*)a == *(float*)b)  //converte o void em float e consulto o conteudo de a e b
        return 0; //se a e b são iguais retorna 0
    else
        if(*(float*)a < *(float*)b)
        return -1; //valor de a vem antes
        else
            return 1; //valor de b vem depois
}

int main()
{
    float *v, aux;
    int n;
    printf("Qual o tamanho do vetor que deseja: ");
    scanf("%d", &n);                                  //escolhe o tamanho do vetor
    v = (float *)calloc(n,sizeof(float));             //alocação de memoria
    for(int i = 0; i < n; i++){
        printf("Digite o elemento da posicao %d: ",i+1);   //digitando os valores do vetor
        scanf("%f", &v[i]);
    }
    qsort(v,n,sizeof(float),comparaCrescente);    //chamada da função, com os argumentos: vetor, tamanho n, tamanho do tipo, os parametros de comparação
    for(int i = 0; i < n; i++){
        printf("%.1f  ", v[i]);    //impressão do vetor organizado
    }
    free(v);     //limpando memoria alocada
    return 0;
}
