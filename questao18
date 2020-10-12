# questao18

#include <stdio.h>
#include <stdlib.h>

float **AlocarMatriz(int m, int n){
    float **v;  //ponteiro para matriz
    v = (float**) calloc (m,sizeof(float *));  //aloca linha das matrizes
    for(int i = 0; i < m; i++){
        v[i] = (float*) calloc(n, sizeof(float));  //aloca as colunas da matriz
    }
    return(v); //retorna o ponteiro para matriz
}

float **LiberaMatriz (int m, int n, float **v){
    for(int i = 0; i <= m; i++){
        free(v[i]);
    }
    free(v);
    return (NULL);

}

void MultiplicaMatriz(int nl3, int nc3, int nl2, float **mat1, float **mat2, float **mat3){
    for(int i = 0; i < nl3; i++){
        for (int j = 0; j < nc3; j++){
            mat3[i][j] = 0;
            for(int k = 0; k < nl2; k++){
                mat3[i][j] += mat1[i][k]*mat2[k][j];
            }
        }
    }

}


int main()
{
   float **mat1, **mat2, **mat3;
   int nc1, nl1, nc2, nl2, nc3, nl3;
    printf("digite o numero de colunas da matriz 1: " );
    scanf("%d", &nc1);
    printf("digite o numero de linhas da matriz 1: " );
    scanf("%d", &nl1);
    printf("digite o numero de colunas da matriz 2: " );
    scanf("%d", &nc2);
    printf("digite o numero de linhas da matriz 2: " );
    scanf("%d", &nl2);
    nl3 = nl1;
    nc3 = nc2;

    mat1 = AlocarMatriz(nl1,nc1);
    mat2 = AlocarMatriz(nl2,nc2);    //alocando memoria
    mat3 = AlocarMatriz(nl3,nc3);

       printf("Preencha a matriz 1: \n");
        for(int i = 0; i < nl1; i++){
            for(int j = 0; j < nc1; j++){     //preenchendo matriz 1
            scanf("%f", &mat1[i][j]);
        }

    }
    printf("Preencha a matriz 2: \n");
        for(int i = 0; i < nl2; i++){
            for(int j = 0; j < nc2; j++){     //preenchendo a matriz 2
            scanf("%f", &mat2[i][j]);
        }

    }
     printf("\n \n");
    for(int i = 0; i < nl1; i++){
        for(int j = 0; j < nc1; j++){        //imprimindo a matriz 1
            printf("%.1f ",mat1[i][j]);

        }
        printf("\n");
    }
    printf("\n \n");
    for(int i = 0; i < nl2; i++){
        for(int j = 0; j < nc2; j++){       //imprimindo a matriz 2
            printf("%.1f ",mat2[i][j]);

        }
        printf("\n");
    }
    printf("\n \n");

    MultiplicaMatriz(nl3, nc3, nl2, mat1, mat2, mat3);

    for(int i = 0; i < nl3; i++){
        for(int j = 0; j < nc3; j++){       //imprimindo a matriz 3
            printf("%.1f ",mat3[i][j]);

        }
        printf("\n");
    }
    LiberaMatriz(nl1, nc1, mat1);
    LiberaMatriz(nl2, nc2, mat2);          //libera a memória
    LiberaMatriz(nl3, nc3, mat3);
    return 0;
}
