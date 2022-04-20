# traversention-in-DS-DAA
#include<stdio.h>
#include<stdlib.h>
#include<conio.h>
//define struct nide type
typedef struct nodetype
{
 int info;
 struct nodetype*next;
}node;
void creatEmptylist(node **head);
void traverseInorder(node *head);
void InsertAtBeginning(node **head,int item);
void deleteFrombegning(node**head);

void main()
{
  node *head;
  int choice,element,after;
  creatEmptylist(&head);
  while(1)
  {
   printf("operation avelable are :");
   printf("1.Insert at begnining\n 2.traverse in order\n enter choice");
   scanf("%d",&choice);
   switch(choice)
   {
    case 1:
    printf("Enter element");
    scanf("%d",&element);
    InsertAtBeginning(&head,element);
    break;

    case 2:
   if(head==NULL)
   printf(" the list is empty");
   else
      traverseInorder(head);
      printf("Press any key to comtinue");
      getch();
          break;
   default:exit(0);
     }
   }
 }
void creatEmptylist(node **head)
{
   *head=NULL;
}
void InsertAtBeginning(node **head, int item)
{
 node *ptr;
 ptr=(node *)malloc(sizeof(node));
 ptr->info=item;
 if(*head==NULL)
  ptr->next=NULL;
 else
 ptr->next=*head;
 *head=ptr;
}
void traverseInorder(node *head)
{
 while(head!=NULL)
 {
 printf("\n %d", head->info);
 head=head->next;
 }
void deleteAtbegning(node**head)
{
  node*REptr;
  if(*head==NULL)
  return;
  else
     ptr=*head
     *head=*head->next;
     free(ptr);
}
}
