
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
ive made a structure named node and then renamed it to NODE using typedef. Now i can use NODE like int, char to declare the structure.

The structure have two parts.
1.Info part
2.NEXT part which is basically pointer to the next NODE
3.First node is called HEAD
4.Last node is called LAST
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


## Insert Operation

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
6. PTR->NEXT=NULL and goto step 
7. Last->NEXT=PTR, PTR->NEXT=NULL, LAST=PTR