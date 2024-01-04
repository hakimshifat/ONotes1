

We have a already declared linked list and a new node. We need to insert the linked list in the linked list.
1. Insert at the end of the linked list
2. Start of the linked list
3. Middle of the linked list


### Inserting at the end of the linked list
#### Algorithm

1. Start
2.  Set PTR = addressof(struct node) (making a new node and allocating space using malloc function)
3. Set PTR->INFO=Value
4. IF(First == Null) goto step 5, else goto step 7
5. First=PTR and Last=PTR
6. PTR->NEXT=NULL 
7. Last->NEXT=PTR, PTR->NEXT=NULL, LAST=PTR

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

  

    NODE *temp = a; // Setting temp to the start of the list

  

    while (temp != NULL)

    {

        printf("%d ->", temp->INFO);

        temp = temp->NEXT;

    }

    int value;

    printf("\nEnter the value to be inserted:");

    scanf("%d", &value);

    NODE *ptr = (NODE *)malloc(sizeof(NODE));

    ptr->INFO = value;

    ptr->NEXT = NULL; // since it will be added at the end of the linked list
    
    if (FIRST == NULL)

    {
      //  a = ptr;

        FIRST = LAST = ptr;
    }

    else

    {

        temp = a;

        while (temp->NEXT != NULL) //will be true when it reaches the end of the linked list

        {
            temp = temp->NEXT;
        }

        temp->NEXT = ptr;

    }
     /* This while operation is most important
    temp will become the first node.
    then it will check which node has NULL pointer... We have not added
    out NEW NODE so the last node of the existing node will have NULL
    pointer. so the TEMP wil become the last node.Then the loop will stop. AND PTR i.e the new node that we want to insert will be linked to the last node.
	 */

    printf("\nAfter insertion the linked list\n");
    
    temp = a; // Resetting temp to the start of the list

    while (temp != NULL)

    {
        printf("%d ->", temp->INFO);

        temp = temp->NEXT;

    }
    printf("END");

    return 0;

}
```
