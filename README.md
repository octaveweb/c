```c
#include <stdio.h>
#include <stdlib.h>

struct node {
    int info;
    struct node *link;
};  

static struct node *first;  

void create() {
    struct node *ptr, *cpt;
    char ch;
    ptr = (struct node *) malloc(sizeof(struct node));

    printf("Enter First node Info: ");
    scanf("%d", &ptr->info);

    first = ptr;

    do {
        cpt = (struct node *) malloc(sizeof(struct node));
        printf("Give the new node Info: ");
        scanf("%d", &cpt->info);
        ptr->link = cpt;
        ptr = cpt;
        printf("Process y/Y for more: ");
        getchar(); 
        scanf("%c", &ch);

    } while (ch == 'y' || ch == 'Y');
    ptr->link = NULL;
}

void display() {
    struct node *ptr = first;
    while (ptr != NULL) {
        printf("%d ", ptr->info);
        ptr = ptr->link;
    }
}

void insertBeginning(){
    struct node *ptr;
    ptr = (struct node *) malloc (sizeof(struct node));

    if(ptr == NULL){
        printf("Overflow");
        exit;
    }else{
       if (first->link == NULL){
       create();
       }else{
        printf("\nCreate new node info: ");
        scanf("%d", &ptr->info);
        ptr->link = first;
        first = ptr;
       }
       
    }
}

int main() {
    int n;
    printf("\n1. Create \t2. Display \t 3. Insert at Bigining");
    printf("\nCreate new node info: ");
    scanf("%d", &n);
switch (n)
{
case 1:
    create();
    break;
    case 2:
    display();
    break;
    case 3:
    insertBeginning();
    break;

default:
printf("Code Treminetrd!");
    break;
}
    
    return 0;
}
```
