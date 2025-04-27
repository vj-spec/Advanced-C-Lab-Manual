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
#define MAX_SIZE 10 

int stack[MAX_SIZE];
int top = -1; 
int isFull() {
    return top == MAX_SIZE - 1;
}
int isEmpty() {
    return top == -1;
}
void push(int element) {
    if (isFull()) {
        printf("Stack is full.\n");
    } else {
        top++;
        stack[top] = element;
        printf("%d pushed onto the stack.\n", element);
    }
}

int peek() {
    if (isEmpty()) {
        printf("Stack is empty.\n");
        return -1; 
    } else {
        printf("Top element of the stack is: %d\n", stack[top]);
        return stack[top];
    }
}

void displayStack() {
    if (isEmpty()) {
        printf("Stack is empty.\n");
    } else {
        printf("\nDisplaying the stack elements\n");
        for (int i = top; i >= 0; i--) {
            printf("%d\n", stack[i]);
        }
    }
}

int main() {
    push(10);
    push(20);
    push(30);
    displayStack();
    peek();

    displayStack();

    return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/c1387258-be58-4c14-ae12-79617b3778b4)


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
#define MAX_SIZE 10 

float stack[MAX_SIZE];
int top = -1; 
int isFull() {
    return top == MAX_SIZE - 1;
}
int isEmpty() {
    return top == -1;
}
void push(float element) {
    if (isFull()) {
        printf("Stack is full.\n");
    } else {
        top++;
        stack[top] = element;
    }
}

int peek() {
    if (isEmpty()) {
        printf("Stack is empty.\n");
        return -1; 
    } else {
        printf("\nTop element of the stack is: %.1f\n", stack[top]);
        return stack[top];
    }
}

void displayStack() {
    if (isEmpty()) {
        printf("Stack is empty.\n");
    } else {
        printf("\nDisplaying the stack elements\n");
        for (int i = top; i >= 0; i--) {
            printf("%.1f\n", stack[i]);
        }
    }
}

int main() {
    push(10.5);
    push(20.5);
    push(30.5);
    displayStack();
    peek();

    displayStack();

    return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/a7b2f2b8-7c5c-4bd9-a60b-dae8f4f53323)

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
        printf("%d enqueued to the queue.\n", element);
    }
}
int dequeue() {
    if (isEmpty()) {
        printf("Queue is empty.\n");
        return -1; 
    } else {
        int dequeuedElement = queue[front];
        front++;
        if (front > rear) {
            front = rear = -1; 
        }
        printf("%d dequeued from the queue.\n", dequeuedElement);
        return dequeuedElement;
    }
}

void displayQueue() {
    if (isEmpty()) {
        printf("Queue is empty.\n");
    } else {
        printf("Queue elements\n");
        for (int i = front; i <= rear; i++) {
            printf("%d\n", queue[i]);
        }
    }
}

int main() {

    enqueue(10);
    enqueue(20);
    enqueue(30);

    displayQueue();

    dequeue();
    displayQueue();

    enqueue(40);
    displayQueue();

    return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/c199ad96-79fe-4f15-8f07-65b553a81a12)


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
        printf("%.1f enqueued to the queue.\n", element);
    }
}

void displayQueue() {
    if (isEmpty()) {
        printf("Queue is empty.\n");
    } else {
        printf("Queue elements\n");
        for (int i = front; i <= rear; i++) {
            printf("%.1f\n", queue[i]);
        }
    }
}

int main() {

    enqueue(10.5);
    enqueue(20.5);
    enqueue(30.5);
    displayQueue();
    enqueue(40.5);
    displayQueue();

    return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/68b64002-9ed0-428d-9284-3515b04f1087)

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
        printf("%d enqueued to the queue.\n", element);
    }
}

int dequeue() {
    if (isEmpty()) {
        printf("Queue is empty.\n");
        return -1; 
    } else {
        int dequeuedElement = queue[front];
        printf("Deleting element: %d from the front of the queue.\n", dequeuedElement);
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
        printf("\nQueue elements\n");
        for (int i = front; i <= rear; i++) {
            printf("%d\n", queue[i]);
        }
    }
}

int main() {

    enqueue(10);
    enqueue(20);
    enqueue(30);
    displayQueue();
    printf("\nDemonstrating Dequeue Operation:\n\n");
    dequeue();
    displayQueue();
    dequeue();
    dequeue();
    displayQueue();
 

    return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/8ab05e96-8ab3-48d8-a9ed-2af009743d37)

Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
