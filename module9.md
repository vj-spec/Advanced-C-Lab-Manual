EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:
```
#include <stdio.h>
#include <stdlib.h>
#define N 10
float stack[N];
int top=-1;
void push(int data)
{
    if(top==N-1)
    {
        printf("\n stack is full\n");
        return;
    }
    stack[++top]=data;
}
int Top(void)
{
    if(top==-1)
        return -1;
    return stack[top];
}
int pop(void)
{
    if(top==-1)
    {
     printf("stack is empty");
    }
    else
    {
     top--;
    }

}
void display(void)
{
    int i;
    for(i=top;i>-1;i--)
        printf("%d\n",stack[i]);
}
void main()
{
   push(10);
   push(20);
   push(30);
   push(40);
   push(50);
   printf("\nstack elements are as follow\n");
   display();
   pop();
   printf("\nAfter pop operation\n");
   display();
   printf("\nThe top value:%d\n",Top());

}
```
Output:

![image](https://github.com/user-attachments/assets/3a9d7c50-ac28-4f6a-8ba4-14df0d91e601)


Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>
#define N 10
float stack[N];
int top=-1;
void push(float data)
{
    if(top==N-1)
    {
        printf("\n stack is full\n");
        return;
    }
    stack[++top]=data;
}
void display(void)
{
    int i;
    for(i=top;i>=1;i--)
        printf("%.1f\n",stack[i]);
}
void main()
{
   push(10.5);
   push(20.5);
   push(30.5);
   push(40.5);
   push(50.5);
   printf("stack elements are as follow\n");
   display();

}
```
Output:

![image](https://github.com/user-attachments/assets/cbd5d948-1728-477b-99a3-e0e175025903)


Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

#define MAX_SIZE 10 

int queue[MAX_SIZE];
int front = -1;
int rear = -1;  

int isFull() {
    return (rear == MAX_SIZE - 1);
}

int isEmpty() {
    return (front == -1 && rear == -1);
}

void enqueue(int element) {
    if (isFull()) {
        printf("Queue is full.\n");
    } else {
        if (isEmpty()) {
            front = 0;
        }
        rear++;
        queue[rear] = element;
    }
}

void dequeue() {
    if (isEmpty()) {
        printf("Queue is empty.\n");
    } else {
        int dequeuedElement = queue[front];
        front++;
        if (front > rear) {
            front = rear = -1; 
        }
    }
}

void displayQueue() {
    if (isEmpty()) {
        printf("Queue is empty.\n");
    } else {
        for (int i = front; i <= rear; i++) {
            printf("%d\n", queue[i]);
        }
    }
}

int main() {
    printf("Elements of the Queue\n");

    enqueue(10);
    enqueue(20);
    enqueue(30);

    displayQueue();

    dequeue();
    printf("After dequeue operation\n");
    displayQueue();

    enqueue(40);
    printf("After enqueue operation\n");
    displayQueue();

    dequeue();
    dequeue();
    dequeue(); 
    printf("After dequeue operation\n");
    displayQueue();

    return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/ff06a6e2-fcbe-4a0c-94cb-5864583af3e4)

Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
```
#include <stdio.h>
#include <stdlib.h>

#define MAX_SIZE 10 

float queue[MAX_SIZE];
int front = -1;
int rear = -1;  

int isFull() {
    return (rear == MAX_SIZE - 1);
}

int isEmpty() {
    return (front == -1 && rear == -1);
}

void enqueue(float element) {
    if (isFull()) {
        printf("Queue is full.\n");
    } else {
        if (isEmpty()) {
            front = 0;
        }
        rear++;
        queue[rear] = element;
    }
}

void dequeue() {
    if (isEmpty()) {
        printf("Queue is empty.\n");
    } else {
        int dequeuedElement = queue[front];
        front++;
        if (front > rear) {
            front = rear = -1; 
        }
    }
}

void displayQueue() {
    if (isEmpty()) {
        printf("Queue is empty.\n");
    } else {
        for (int i = front; i <= rear; i++) {
            printf("%.1f\n", queue[i]);
        }
    }
}

int main() {
    printf("Elements of the Queue\n");
    enqueue(10.5);
    enqueue(20.5);
    enqueue(30.5);
    displayQueue();

    dequeue();
    printf("After dequeue operation\n");
    displayQueue();

    return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/7cea07aa-84df-473c-8f5d-7e52284c1ea3)

Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:
```
#include <stdio.h>
#include <stdlib.h>

#define MAX_SIZE 10 

int queue[MAX_SIZE];
int front = -1; 
int rear = -1;  

int isEmpty() {
    return (front == -1 && rear == -1);
}

void enqueue(int element) {
    if (rear == MAX_SIZE - 1) {
        printf("Queue is full.\n");
    } else {
        if (front == -1) {
            front = 0;
        }
        rear++;
        queue[rear] = element;
    }
}

int dequeue() {
    if (isEmpty()) {
        printf("Queue is empty.\n");
        return -1; 
    } else {
        int dequeuedElement = queue[front];
        printf("Deleting element: %d \n", dequeuedElement);
        front++;
        if (front > rear) {
            front = rear = -1; 
        }
        return dequeuedElement;
    }
}

void displayQueue() {
    if (isEmpty()) {
        printf("Queue is empty.\n");
    } else {
        for (int i = front; i <= rear; i++) {
            printf("%d\n", queue[i]);
        }
    }
}

int main() {
    printf("Demonstrating Dequeue Operation:\n");

    enqueue(10);
    enqueue(20);
    enqueue(30);

    displayQueue();

    dequeue();
    displayQueue();

    dequeue();
    dequeue();
    displayQueue();

    dequeue(); // Try to dequeue from an empty queue

    return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/eeff19f6-755d-4188-a16d-12a762a1a27d)

Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
