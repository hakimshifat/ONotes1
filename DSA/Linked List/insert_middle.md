```C
#include <stdio.h>

#include <stdarg.h>

#include <stdlib.h>

  

struct node

{

    int INFO;

    struct node *NEXT;

};

  

typedef struct node NODE;

  

void printfLL(NODE *head);

void insert_middle(NODE *head, int position, int value);

  

int main()

{

    NODE *a = NULL;

    NODE *b = NULL;

    NODE *c = NULL;

  

    a = (NODE *)malloc(sizeof(NODE));

    b = (NODE *)malloc(sizeof(NODE));

    c = (NODE *)malloc(sizeof(NODE));

  

    a->INFO = 10;

    b->INFO = 20;

    c->INFO = 30;

  

    a->NEXT = b;

    b->NEXT = c;

    c->NEXT = NULL;

  

    NODE *FIRST = a;

    NODE *LAST = c;

  

    printfLL(FIRST);

  

    int value, position;

    printf("\nEnter the value to be inserted at Middle of the list:");

    scanf("%d", &value);

    printf("\nEnter the position:");

    scanf("%d", &position);

    insert_middle(FIRST,position,value);

    printfLL(FIRST);

  

    return 0;

}

  

void printfLL(NODE *head)

{

    while (head != NULL)

    {

        printf("%d ->", head->INFO);

        head = head->NEXT;

    }

    printf("NULL");

}

void insert_middle(NODE *head, int position, int value)

{

    NODE *temp = head;

    int counter = 0;

    while (temp != NULL)

    {

        counter++;

        if (counter == position)

        {

            NODE *NewNode = (NODE *)malloc(sizeof(NODE));

            NewNode->INFO = value;

            NewNode->NEXT = temp->NEXT;

            temp->NEXT = NewNode;

        }

        temp = temp->NEXT;

    }

}
```