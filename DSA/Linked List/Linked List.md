
Declaration:

```c
#include<stdio.h>
int main()
{

typedef struct node NODE{
int INFO;
struct node *NEXT;
};

return 0;
}
```
I've made a structure named node and then renamed it to NODE using typedef. Now i can use NODE like int, char to declare the structure.

The structure have two parts.
1.Info part
2.NEXT part which is basically pointer to the next NODE
3.First node is called HEAD
4.Last node is called LAST.
5.The NEXT part of LAST will be NULL.

```C
#include <stdio.h>

#include <stdlib.h>

int main()

{

    struct node

    {

        int INFO;

        struct node *NEXT;

    };
    // Made a structure

    typedef struct node NODE;
    // Renamed it NODE

    NODE *a = NULL;

    NODE *b = NULL;

    NODE *c = NULL;
    //Declared 3 nodes that are empty
    // They are in POINTER format  

    a = (NODE *)malloc(sizeof(NODE));

    b = (NODE *)malloc(sizeof(NODE));

    c = (NODE *)malloc(sizeof(NODE));
   //Allocated space for them using malloc
   // Their type would be NODE POINTER

    a->INFO = 10;

    b->INFO = 20;

    c->INFO = 30;
    //Assigning value
    a->NEXT = b;

    b->NEXT = c;

    c->NEXT = NULL;
    //making connection between nodes

    while (a != NULL)

    {

        printf("%d ->", a->INFO);

            a = a->NEXT;

    }
    //printing nodes
    return 0;

}
```



