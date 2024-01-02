```C
#include <stdio.h>

#include <stdlib.h>

struct node

{

    int data;

    struct node *next;

};

// making linked list structure

  

typedef struct node Node; // gonna use Node instead of "struct node"

  

Node *createlinkedlist(int arr[], int size);

  

int main()

{

   // printf("This function will create a new linked list from array");

    int a[] = {1, 2, 4};

    Node *head;

    head = createlinkedlist(a, 3);

  

    while (head != NULL)

    {

        printf("%d -> ", head->data);

        head = head->next;

    }

  

    printf("NULL");

  

    return 0;

}

Node *createlinkedlist(int arr[], int size)

{

    Node *head = NULL, *temp = NULL, *current = NULL;

    for (int i = 0; i < size; i++)

    {

  

        temp = (Node *)malloc(sizeof(Node)); // taking space for temp;

        temp->data = arr[i];

        temp->next = NULL;

  

        if (head == NULL)

        {

            head = temp; // will take temps data and next and put them in heads vault

            current = temp;

        }

        else

        {

            current->next = temp;

            current = current->next;

        }

    }

    return head;

}
```