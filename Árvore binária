#include <stdlib.h>
#include <stdio.h>

typedef struct node{
    int chave;
    int h;
    struct node *esq;
    struct node *dir;
}Tnode;

Tnode* inicia(int x){
    Tnode *novo= (Tnode*)malloc(sizeof(Tnode));
        novo->chave=x;
        novo->h=0;
        novo->esq= NULL;
        novo->dir= NULL;
return novo;
}
Tnode* insere(Tnode *arvore, int x){
    if(arvore== NULL){
        arvore=inicia(x);
    return arvore;
    }
    while(arvore->chave)



}

void imprimeEDR( Tnode *arvore){
    imprimeEDR(arvore->esq);
    imprimeEDR(arvore->dir);
    printf("%d", arvore->chave);
}

void pesquisar( Tnode *arvore, int x){
    if(arvore->chave==x){
        printf("presente");
    }
    else{
        pesquisar(arvore->esq, x);
        pesquisar(arvore->dir, x);
    }
printf("Nao encontrado");
}

int main(void){
    Tnode* arvore=(Tnode*)malloc(sizeof(Tnode));


}
