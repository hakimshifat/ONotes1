
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


## Insert Operation

We have a already declared linked list and a new node. We need to insert the linked list in the linked list.
1. Insert at the end of the linked list
2. Start of the linked list
3. Middle of the linked list


### Inserting at the end of the linked list
#### Algorithm

