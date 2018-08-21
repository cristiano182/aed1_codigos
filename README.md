

#include <stdlib.h>
#include <stdio.h>

struct cadastro
{
   char nome[30];
   char cpf[11];
};

typedef struct cadastro PESSOA;

int main()
{

    int i,tam;
    PESSOA *ponteiroPessoa;

    printf("Digite o tamanho do vetor para alocação: \n");
    scanf("%d", &tam);
    
    ponteiroPessoa = (PESSOA *)malloc(tam*sizeof(PESSOA));

    for(i=0; i<tam; i++)
    {
          printf("Insira o Nome: \n");
          getchar();
          gets(ponteiroPessoa[i].nome);

          printf("Insira o CPF com 11 Digitos: \n");
          getchar();
          gets(ponteiroPessoa[i].cpf);
    }

    for(i=0; i<tam; i++)
    {
         printf("Nome: %s - CPF: %s \n", ponteiroPessoa[i].nome,ponteiroPessoa[i].cpf);
    }

    free(ponteiroPessoa);

    return 0;
}
