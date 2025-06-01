## EXP NO 3A : C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

## Aim:
To write a C program to display stack elements using an array.

## Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
## Program:
~~~
float stack[100];
int top;
void display()
{
    for(int i=top;i>=0;i--)
    {
        printf("%.1f ",stack[i]);
    }
}
~~~
## Output:
![Screenshot 2025-06-01 231821](https://github.com/user-attachments/assets/38a0e9a2-7aab-4147-9373-6bc792cdbae1)


## Result:
Thus, the program to display stack elements using an array is verified successfully.
 


## EXP NO 3B : PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.

## Aim:
To create a C program to push the given element in to a stack using array.

## Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
## Program:
~~~
int size=3,top=-1;
char stack[100];
void push (char data)
{
      if(top>=size-1)
      {
          printf("stack is full\n");
      }
      else
      {
          stack[++top]=data;
      }
}
~~~
## Output:
![Screenshot 2025-06-01 231923](https://github.com/user-attachments/assets/dcb1339e-d6b4-43e5-af33-b35add5ace65)

## Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
## EXP NO 3C : C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.

## Aim:
To write a C program to display queue elements using array

## Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
## Program:
~~~
int front;
int rear;
char queue[50];
void display()
{
     if(front==-1)
    {
        printf("No elements to display");
    }
    else
    {
    for (int i=front;i<=rear;i++)
    {
        printf("%c ",queue[i]);
    }
    }
}
~~~
## Output:
![Screenshot 2025-06-01 232006](https://github.com/user-attachments/assets/376f1017-3dd0-4bcb-86b9-0b5f51f9b41d)
## Result:
Thus, the program to display queue elements using array is verified successfully.


 
## EXP NO 3D : C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.

## Aim:
To write a C program to insert elements in queue using array.

## Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

## Program:
~~~
int size=4, rear=-1, front=-1; 
float queue[50];
void enqueue(float data)
{
    if(rear<size)
    {
        if(front==-1)
        {
            front=0;
        }
        rear=rear+1;
        queue[rear]=data;
        
    }
}
~~~

## Output:
![Screenshot 2025-06-01 232051](https://github.com/user-attachments/assets/a1c6d37b-c6bb-430a-9256-682df043027c)

## Result:
Thus, the program to insert elements in queue using array is verified successfully.



 ## EXP NO 3E : C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY

## Aim:
To create a function in C that deletes an element from a queue implemented using an array.

## Algorithm:
1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.

## Program:
~~~
int front, rear;
void dequeue()
{
    if(front==-1)
    {
        printf("No elements to display");
    }
    else if (front==rear)
    {
        
        front=rear=-1;
    }
    else
    {
        front++;
    }
}
~~~

## Output:
![Screenshot 2025-06-01 232143](https://github.com/user-attachments/assets/74200412-e1be-4be3-bf1e-e738bdbfd570)

## Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
