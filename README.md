# Stacks-

A stack is a linear data structure that consists of a group of identical elements.

A stack only has one endpoint where components can be added or removed. "Last In, First Out" (LIFO) is a term used to explain how a stack behaves. The first thing to be "popped" off of the stack when an element is "pushed" onto it is that element. You must pop every preceding item in order to get to the oldest inputted item.

![image](https://user-images.githubusercontent.com/91966097/234320022-25f492de-28d8-484d-bc37-def2b8c54a02.png)

Operations Performed on Stacks

The following are the fundamental functions that stacks support.

Push: Adds a component to the stack's top.

pop: Removes the topmost stack element.

check whether the stack is empty with isEmpty.

isFull: Determines if the stack is completely full.

top: Shows the stack's topmost element.

To maintain track of the item at the top of the stack, a pointer called top is first set. The stack has a -1 initialization.

The stack is then checked to see if it is empty by comparing top to -1.

The top of the stack is updated when new pieces are added.

The topmost element is eliminated and the position of top is updated as soon as items are popped or removed.

Program to push/pop an element in a stack

            #include <stdio.h>

            void push(int);
            void pop();
            void display();

            int stack[10];
            int top = -1;
            int data;

            int main() {
                int choice;
                do {
                    printf("\n 1. Push \n 2. Pop \n 3. Display \n");
                    scanf("%d", &choice);
                    if (choice == 1) {
                        scanf("%d", &data);
                        push(data);
                    } else if (choice == 2) {
                        pop();
                    } else if (choice == 3) {
                        display();
                    } else {
                        printf("Invalid input");
                    }
                } while (choice != 0);
            }

            void push(int data) {
                if (top == 9) {
                    printf("overflow");
                } else {
                    top = top + 1;
                    stack[top] = data;
                }
            }

            void pop() {
                if (top == -1) {
                    printf("underflow");
                } else {
                    top = top - 1;
                }
            }

            void display() {
                int i;
                if (top == -1) {
                    printf("Stack is empty");
                } else {
                    for (i = top; i >= 0; i--) {
                        printf("\n %d", stack[i]);
                    }
                }
            }
 The element that was put last is the first one to be deleted in a stack, which is a linear data structure that adheres to the Last In First Out (LIFO) concept. Push, Pop, and Display are the three operations the user may carry out using the program's menu-driven interface.
The primary function calls the associated function after reading the user's selection from the menu. An error warning appears if the user enters a number other than 1, 2, or 3.
If the stack is not full, the push function accepts an integer as input and adds it to the top of the stack. If not, an overflow error notice is displayed.
If the stack is not empty, the pop function eliminates the element at the top. If not, an underflow error notice is displayed.
If the stack is not empty, the show function prints the stack's items from top to bottom. If not, a message stating that the stack is empty is displayed.
The user's input determines the program's output.


