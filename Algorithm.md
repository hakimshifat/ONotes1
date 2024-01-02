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
13. then if will check again step 10 but it will become false and will do the else statement
14. 