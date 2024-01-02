1. Start
2. Make structure function of linked list outside main function
3. Declaring a Node type function that takes an array with its size and returns the head of the linked list with is a node.
4.  Declare 3 Pointer node. Head, temp, Current
5. Start an array that will run run as the size of the array(think of printing the array and then throw away the print function)
6. Allocate space for TEMP using malloc function and typecaste it to Node pointer
7. Store the first element of the array into temp.data
8. and store NULL into temp.next
9. right now, head and current is null but temp has values
10. IF (HEAD== NULL) //it will become true
11.  head=temp and current=temp
12. now head, temp, current all has values and all are the first element of the array and NEXT is NULL in all Nodes
13. then the loop will start again but for the 2nd element
14.  temp.data will hold the 2nd element and temp.next will hold NULL
15. if statement will become false and execute the else statement
16.  Now current holds the previous temp values which is the same values set in head. So current->next will mean another node after head which will be created automatically and will hold the current temp values.
17. Then current will be set to second node.
18. after the loop is finished, the function will return only head
19. Then in the main function, we will make a node pointer and store the returning value of the function in it. Then use it to print the linked list.