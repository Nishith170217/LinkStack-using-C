#include<stdio.h>
#include<stdlib.h>
#define OK 1

typedef struct stack{
   int data;
   struct stack* next;

}sqStack;
sqStack *top=NULL;

void push(int);
void pop();
void display();

void main()
{
   int choice, value;

   printf("\n\t::Stack Operations::\n");
   while(1){
      printf("************************************\n");
      printf("*  Lab 2 by Nishith (10460348058)  *\n");
      printf("************************************\n");
      printf("*    Choose 1-4                    *\n");
      printf("*   1.Push                         *\n");
      printf("*   2.Pop                          *\n");
      printf("*   3.Display                      *\n");
      printf("*   4.Exit                         *\n");
      printf("************************************\n");
      scanf("%d",&choice);
      switch(choice){
	 case 1:
          printf("Enter the value to be insert: ");
          scanf("%d", &value);
          push(value);
          break;
	 case 2:
	      pop();
	      break;
	 case 3:
	      printf("\n** Current Stack is **\n");
	      display();
          break;
	 case 4:
	      exit(OK);
	 default:
	      printf("\nPlease Enter the Correct Number \n");
      }
   }
}
void push(int value)
{
   sqStack *newNode;
   newNode = (sqStack*)malloc(sizeof(sqStack));
   newNode->data = value;
   if(top == NULL)
      newNode->next = NULL;
   else
      newNode->next = top;
   top = newNode;
   printf("\nSuccessfully Inserted!\n");
}
void pop()
{
   if(top == NULL)
      printf("\nStack is Empty!!!\n\n");
   else{
      sqStack* temp;
      temp = top;
      printf("\nPopped element: %d\n\n", temp->data);
      top = temp->next;
      free(temp);
   }
}
void display()
{
   if(top == NULL)
      printf("\nStack is Empty!!!\n\n");
   else{
      sqStack* temp;
      temp = top;
      printf("----------------------\n");
      while(temp->next != NULL)
      {
        printf("\t%d\n",temp->data);
        printf("----------------------\n");
        temp = temp -> next;
      }
      printf("\t%d\n",temp->data);
      printf("----------------------\n");
   }
}
