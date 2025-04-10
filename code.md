# Link list 
> ##  Write a program to create a link list.


```c
#include <stdio.h>
#include <stdlib.h>

struct node {
    int info;
    struct node *link;
};

struct node *first = NULL;

void create() {
    struct node *ptr, *cpt;
    char ch;
    ptr = (struct node *) malloc(sizeof(struct node));

    if (!ptr) {
        printf("Memory allocation failed\n");
        return;
    }

    printf("Enter First node Info: ");
    scanf("%d", &ptr->info);
    ptr->link = NULL;
    first = ptr;

    do {
        cpt = (struct node *) malloc(sizeof(struct node));
        if (!cpt) {
            printf("Memory allocation failed\n");
            return;
        }

        printf("Give the new node Info: ");
        scanf("%d", &cpt->info);
        cpt->link = NULL;
        ptr->link = cpt;
        ptr = cpt;

        printf("Process y/Y for more: ");
        getchar(); // consume leftover newline
        scanf("%c", &ch);

    } while (ch == 'y' || ch == 'Y');
}

void display() {
    struct node *ptr = first;
    if (first == NULL) {
        printf("List is empty\n");
        return;
    }

    printf("Linked List: ");
    while (ptr != NULL) {
        printf("%d ", ptr->info);
        ptr = ptr->link;
    }
    printf("\n");
}

void insertBeginning() {
    struct node *ptr = (struct node *) malloc(sizeof(struct node));

    if (ptr == NULL) {
        printf("Overflow\n");
        exit(1);
    }

    printf("Create new node info: ");
    scanf("%d", &ptr->info);
    ptr->link = first;
    first = ptr;
}

int main() {
    int n;
    while (1) {
        printf("\n1. Create \t2. Display \t3. Insert at Beginning \t4. Exit");
        printf("\nEnter choice: ");
        scanf("%d", &n);

        switch (n) {
            case 1:
                create();
                break;
            case 2:
                display();
                break;
            case 3:
                insertBeginning();
                break;
            case 4:
                exit(0);
            default:
                printf("Invalid option\n");
        }
    }
    return 0;
}
```
