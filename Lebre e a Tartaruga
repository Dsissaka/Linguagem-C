
#include <stdlib.h>
#include <stdio.h>
#include <locale.h>
#include <time.h>

typedef struct node{
    int posicao;
    struct node *prox;
}Tnode;

Tnode* inicia(int x){
    Tnode* novonode= (Tnode*)malloc(sizeof(Tnode));
    if(novonode!= NULL){
        novonode->posicao=x;
    novonode->prox=NULL;
    }else{
    printf("Aloca��o mal-sucedida\n");
    }
return novonode;
}
Tnode* inserefim(Tnode *cabeca, int x){
    Tnode *novonode=inicia(x);
    if(novonode==NULL){
        printf("Aloca��o mal-sucedida\n");
    }else{
    novonode->prox=cabeca;
    }

return novonode;
}

void limpa (Tnode *node){
    Tnode* Node= node;
    if(Node!= NULL){
        return;
    }else{
    Tnode* prox;
        if(prox==NULL){
                while(Node!=NULL){
            prox=Node->prox;
            free(Node);
            Node=prox;
        }

            }else{
        printf("Aloca��o mal-sucedida\n");
        }
    }
}

void movimento_tarta(Tnode *Tartaruga, FILE *arquivo){
    int min=1, max=10;
    int dado= rand() % (max-min+1)+ min;
        if(dado<=5){
        fprintf(arquivo ,"A tartaruga andou uma casa\n");
        printf("A tartaruga andou uma casa\n");
            Tartaruga->posicao++;
            return;
        }else{
            if(dado<=9){
                fprintf(arquivo, "A tartaruga n�o andou nenhuma casa\n");
                printf("A tartaruga n�o andou nenhuma casa\n");
                return;
            }else{
                fprintf(arquivo, "A tartaruga retornou uma casa\n");
                printf("A tartaruga retornou uma casa\n");
                Tartaruga->posicao--;
                if(Tartaruga->posicao<1){
                    Tartaruga->posicao=1;
                }
            return;
            }
        }
}

void movimento_lebre(Tnode *Lebre, FILE *arquivo){
    int min=1, max=10;
    int dado= rand() % (max-min+1)+ min;
        if(dado<=4){
        fprintf(arquivo, "A lebre andou uma casa\n");
        printf("A lebre andou uma casa\n");
            Lebre->posicao++;
            return;
        }else{
            if(dado<=8){
                fprintf(arquivo, "A Lebre n�o andou nenhuma casa\n");
                printf("A Lebre n�o andou nenhuma casa\n");
                return;
            }else{
                fprintf(arquivo, "A Lebre retornou uma casa\n");
                printf("A Lebre retornou uma casa\n");
                Lebre->posicao--;
                if(Lebre->posicao<1){
                    Lebre->posicao=1;
                }
            return;
            }
        }
}

int main(void){
    FILE *arquivo = fopen( "arquivo.txt", "w");
    setlocale(LC_ALL, "Portuguese");
    srand(time(NULL));
    int loop;
    Tnode *Lebre = inicia(1);
    Tnode *Tartaruga= inicia(1);
        while(Lebre->posicao<70 && Tartaruga->posicao<70){
            movimento_lebre(Lebre, arquivo);
            movimento_tarta(Tartaruga, arquivo);
            printf("Atual posi��o da tartaruga: %d\n", Tartaruga->posicao);
            fprintf(arquivo ,"Atual posi��o da tartaruga: %d\n", Tartaruga->posicao, arquivo);
            printf("Atual posi��o da lebre: %d\n", Lebre->posicao);
            fprintf(arquivo ,"Atual posi��o da lebre: %d\n", Lebre->posicao, arquivo);
            loop++;
            printf("Fim do %d loop\n__________________________________________________\n", loop);
            fprintf(arquivo ,"Fim do %d loop\n__________________________________________________\n", loop, arquivo);
        }
    if(Lebre->posicao==70){
            fprintf(arquivo ,"\nA lebre ganhou\n\nEncerrando...\n", arquivo);
            printf("\nA lebre ganhou\n\nEncerrando...\n");

        }
    if(Tartaruga->posicao==70){
            fprintf(arquivo ,"\nA tartaruga ganhou\n\nEncerrando...\n");
            printf("\nA tartaruga ganhou\n\nEncerrando...\n");
        }
    fclose (arquivo);
    limpa(Tartaruga);
    limpa(Lebre);
return 155;
}

