

```C
#include <stdio.h>

#include <stdarg.h>

#include <stdlib.h>

  

int main()

{

    struct node

    {

        int INFO;

        struct node *NEXT;

    };

    typedef struct node NODE;

    NODE *a = NULL;

    NODE *b = NULL;

    NODE *c = NULL;

   // NODE *FIRST = a;

    //NODE *LAST = c;

  

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
   //This must be declared last of connecting the nodes

  

    if (a == NULL) //checking for empty list

    {

        printf("Empty LIST");

    }

    else if (FIRST == LAST) //Checking for one element

    {

        printf("\n%d->", FIRST->INFO);

    }

    else //real work happens here

    {

        NODE *temp = FIRST; // using temp for not messing with the originial linked connection

        while (temp != NULL)

        {

            printf("%d->", temp->INFO);

                temp = temp->NEXT;

        }

    }

printf("\n\nUSING YOUTUBE METHOD\n");

    while (a != NULL)

    {

        printf("%d ->", a->INFO);

        a = a->NEXT;

    }

  

    return 0;

}
```

