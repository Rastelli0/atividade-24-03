#include <stdio.h>

int main(){
    
    float matriz[3][3],  soma_mat, media, maior, menor, media_sec ; 
  int i, j, veri, soma_sec = 0, par_sec, imp_prin = 0,  soma_prin = 0, diff;

for( i = 0; i < 3; i++){
  printf("\n");
    for( j = 0; j < 3; j++){
        printf("Digite os valores da matriz: ");
        scanf("%f", &matriz[i][j]);


    }
}
printf("matriz:");
for(i = 0; i < 3; i++){
    printf("\n");
      for(j = 0; j < 3; j++){
       
          printf(" %2.0f \t", matriz[i][j]);
  
  
      }
  }
maior = matriz[1][1];
menor = matriz[1][1];
  for(i = 0; i < 3; i++){
    printf("\n");
      for(j = 0; j < 3; j++){
          soma_mat += matriz[i][j];
          if(matriz[i][j] > maior){
            maior = matriz[i][j];
          }else if(matriz[i][j] < menor){
            menor = matriz[i][j];
          }
      }
  }


printf("\n soma da matriz: %2.0f", soma_mat);

media = (soma_mat / 9);

printf("\n media: %2.0f", media);

printf("\n maior:%2.0f / menor: %2.0f", maior ,menor);

for(i = 0; i < 3; i++){
    printf("\n");
          soma_sec += matriz[i][2-i];
             veri = matriz[i][2-i];
          if(veri % 2 == 0){
            par_sec++;
          }
      
}
media_sec = (soma_sec / 3);

printf("\n media dig secundaria: %2.0f", media_sec);

printf("\n pares dig secundaria: %d", par_sec);


for(i = 0; i < 3; i++){
    printf("\n");
    soma_prin += matriz[i][i];
             veri = matriz[i][i];
          if(veri % 2 != 0){
            imp_prin +=1;
          }
      
}
printf("\n impares dig principal: %d", imp_prin);

diff =  soma_prin - soma_sec;

printf("\n Diferença da somatoria: %d", diff);



return 0;
}
