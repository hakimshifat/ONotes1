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

  

void printlinkedlist(NODE *head)

{

    while (head != NULL)

    {

        printf("%d ->", head->INFO);

        head = head->NEXT;

    }

    printf("NULLL");

}

  

void insert_end(int value, NODE *FIRST)

{

    NODE *temp = FIRST; // Setting temp to the start of the list

    NODE *ptr = (NODE *)malloc(sizeof(NODE));

    ptr->INFO = value;

    ptr->NEXT = NULL; // since it will be added at the end of the linked list

  

    if (FIRST == NULL)

    {

        FIRST = ptr;

    }

    else

    {

        temp = FIRST;

        while (temp->NEXT != NULL) // will be true when it reaches the end of the linked list

        {

            temp = temp->NEXT;

        }

        temp->NEXT = ptr;

    }

}

void insert_start(int value, NODE *FIRST)

{

    NODE *temp = (NODE *)malloc(sizeof(NODE));

    temp->INFO = value;

    temp->NEXT = FIRST;

    NODE *head = temp;

    printf("After inserting at the start of the list\n");

    printlinkedlist(head);

}

  

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

  

    printlinkedlist(FIRST);

  

    int value;

    printf("\nEnter the value to be inserted at End of the list:");

    scanf("%d", &value);

  

    printf("\nAfter insertion the linked list\n");

  

    insert_end(value, FIRST);

  

    printlinkedlist(FIRST);

  

    printf("\nEnter the value that you want to start at the START:");

    int value1;

    scanf("%d", &value1);

    insert_start(value1, FIRST);

  

    return 0;

}
```