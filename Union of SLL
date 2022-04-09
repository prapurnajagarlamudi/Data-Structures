#include<stdio.h>
#include<stdlib.h>
struct node
{
    int data;
    struct node* next;
}*newnode,*temp,*head1,*head2;
struct node* head=NULL;
struct node* tail=NULL;

// creation of a single linked list
struct node* create (struct node* head)
{
    char ch;
    int value;
    do
    {
    newnode=(struct node*)malloc(sizeof(struct node));
    printf("enter the value");
    scanf("%d",&value);
    newnode->data=value;
    newnode->next=NULL;
    if(head==NULL)
    {
        head=newnode;
        tail=newnode;
    }
    else
    {
        tail->next=newnode;
        tail=newnode;
    }
    printf("enter e to exit and c to continue");
    scanf(" %c",&ch);
    }
    while(ch == 'c');
    return head;
}

// display of a single linked list
void display(struct node* head)
{
    temp=head;
    while(temp!=NULL)
    {
    printf("%d\n",temp->data);
    temp=temp->next;
    }
}

struct node* concatenation (struct node head1,struct node head2) 
{
    struct node *temp1 = head1, *temp2 = head2;
    while(temp1->next!=NULL)
    {
        temp1=temp1->next;
    }
    temp1->next=head2;
    return head1;
} 
 
void sort(struct node *head)
{
    int var;
    struct node* i,*j;
    temp=head;
    for(i=temp;i->next!=NULL;i=i->next)
    {
        for(j=i->next;j!=NULL;j=j->next)
        {
            if(i->data > j->data)
            {
                var=i->data;
                i->data=j->data;
                j->data=var;
            }
        }
    }
}
 
void delete(struct node* head) 
{
    struct node *temp=head,*temp1;
    while (temp->next != NULL)
    {
        temp1=temp-> next;
        if(temp1->data ==temp->data)
        {
            temp->next = temp->next->next;
        }
        temp=temp->next;
    }
}

void main()
{
    struct node *h1,*h2,*h3;
    printf("enter 1st list:");
    h1=create(head1);
    
    printf("enter 2nd list:");
    h2=create(head2);
    
    printf("1st list:");
    display(h1);
    
    printf("2nd list:");
    display(h2);
    
    printf("union:");
    h3=concatenation(h1,h2);
    sort(h3);
    delete(h3);
    display(h3);
}
