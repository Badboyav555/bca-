# DATA STRUCTURES AND ALGORITHMS

# UNIT – LINKED LIST

---

# Introduction to Linked List

Linked List:
```text
Dynamic Linear Data Structure
```
hai jisme:
- elements memory mein continuously store nahi hote
- har element next element ka address store karta hai

---

# Why Linked List Needed

Array mein:
- fixed size problem hoti hai
- insertion/deletion difficult hoti hai

Linked List:
```text
In problems ko solve karti hai
```

---

# Real Life Example

Suppose:
- train ke bogies

Har bogie:
- next bogie se connected hoti hai

Agar ek bogie remove/add karni ho:
- easily possible hai

Isi tarah:
```text
Linked List
```
work karti hai.

---

# Basic Structure of Linked List

Linked list ka har element:
```text
Node
```
kehlata hai.

Har node mein:
1. Data
2. Address of next node

store hota hai.

---

# Node Representation

```md
![Linked List Node](images/linked-list-node.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/6/6d/Singly-linked-list.svg

---

# Structure of Node in C

```c
struct node
{
    int data;
    struct node *next;
};
```

---

# Components of Linked List

1. Node
2. Data
3. Pointer
4. Head Pointer

---

# Head Pointer

Linked list ka first node:
```text
Head Pointer
```
store karta hai.

---

# Advantages of Linked List

1. Dynamic size
2. Easy insertion
3. Easy deletion
4. Better memory utilization

---

# Disadvantages

1. Extra memory for pointer
2. Sequential access only
3. Traversal slow

---

# Types of Linked List

1. Singly Linked List
2. Doubly Linked List
3. Circular Linked List

---

# SINGLY LINKED LIST

# Introduction

Singly Linked List mein:
```text
Har node sirf next node ka address store karti hai
```

---

# Structure

```text
DATA | NEXT
```

---

# Image Representation

```md
![Singly Linked List](images/singly-linked-list.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/6/6d/Singly-linked-list.svg

---

# Example of Singly Linked List

```text
10 -> 20 -> 30 -> NULL
```

---

# Working of Singly Linked List

- First node:
```text
HEAD
```
ke through access hoti hai.

- Last node ka next:
```text
NULL
```
hota hai.

---

# C Program to Create Singly Linked List

```c
#include<stdio.h>
#include<stdlib.h>

struct node
{
    int data;
    struct node *next;
};

struct node *head=NULL;

void create()
{
    struct node *newnode,*temp;
    int value,choice=1;

    while(choice)
    {
        newnode=(struct node*)malloc(sizeof(struct node));

        printf("Enter Data:");
        scanf("%d",&value);

        newnode->data=value;
        newnode->next=NULL;

        if(head==NULL)
        {
            head=newnode;
        }
        else
        {
            temp=head;

            while(temp->next!=NULL)
            {
                temp=temp->next;
            }

            temp->next=newnode;
        }

        printf("Press 1 to continue:");
        scanf("%d",&choice);
    }
}
```

---

# Display Linked List Program

```c
void display()
{
    struct node *temp;

    temp=head;

    while(temp!=NULL)
    {
        printf("%d -> ",temp->data);
        temp=temp->next;
    }

    printf("NULL");
}
```

---

# Complete Program

```c
#include<stdio.h>
#include<stdlib.h>

struct node
{
    int data;
    struct node *next;
};

struct node *head=NULL;

void create()
{
    struct node *newnode,*temp;
    int value,choice=1;

    while(choice)
    {
        newnode=(struct node*)malloc(sizeof(struct node));

        printf("Enter Data:");
        scanf("%d",&value);

        newnode->data=value;
        newnode->next=NULL;

        if(head==NULL)
        {
            head=newnode;
        }
        else
        {
            temp=head;

            while(temp->next!=NULL)
            {
                temp=temp->next;
            }

            temp->next=newnode;
        }

        printf("Press 1 to continue:");
        scanf("%d",&choice);
    }
}

void display()
{
    struct node *temp;

    temp=head;

    while(temp!=NULL)
    {
        printf("%d -> ",temp->data);
        temp=temp->next;
    }

    printf("NULL");
}

void main()
{
    create();
    display();
}
```

---

# Output

```text
Enter Data:10
Press 1 to continue:1

Enter Data:20
Press 1 to continue:1

Enter Data:30
Press 1 to continue:0

10 -> 20 -> 30 -> NULL
```

---

# Inserting Element in Linked List

# Introduction

New node ko linked list mein add karna:
```text
Insertion
```
kehlata hai.

---

# Types of Insertion

1. Insertion at Beginning
2. Insertion at End
3. Insertion at Specific Position

---

# Insertion at Beginning

# Algorithm

1. Create new node
2. New node ka next = head
3. Head = new node

---

# Program

```c
void insert_begin()
{
    struct node *newnode;
    int value;

    newnode=(struct node*)malloc(sizeof(struct node));

    printf("Enter Data:");
    scanf("%d",&value);

    newnode->data=value;

    newnode->next=head;

    head=newnode;
}
```

---

# Insertion at End

# Algorithm

1. Create node
2. Traverse till last node
3. Last node next = new node

---

# Program

```c
void insert_end()
{
    struct node *newnode,*temp;
    int value;

    newnode=(struct node*)malloc(sizeof(struct node));

    printf("Enter Data:");
    scanf("%d",&value);

    newnode->data=value;
    newnode->next=NULL;

    temp=head;

    while(temp->next!=NULL)
    {
        temp=temp->next;
    }

    temp->next=newnode;
}
```

---

# Deleting Element in Linked List

# Introduction

Node remove karna:
```text
Deletion
```
kehlata hai.

---

# Types of Deletion

1. Delete from Beginning
2. Delete from End
3. Delete Specific Node

---

# Delete from Beginning

# Algorithm

1. Temp = head
2. Head = head->next
3. Free temp

---

# Program

```c
void delete_begin()
{
    struct node *temp;

    temp=head;

    head=head->next;

    free(temp);

    printf("First Node Deleted");
}
```

---

# Delete from End

# Program

```c
void delete_end()
{
    struct node *temp,*prev;

    temp=head;

    while(temp->next!=NULL)
    {
        prev=temp;
        temp=temp->next;
    }

    prev->next=NULL;

    free(temp);

    printf("Last Node Deleted");
}
```

---

# Searching in Linked List

# Introduction

Specific element ko find karna:
```text
Searching
```
kehlata hai.

---

# Real Life Example

Suppose:
- student record list mein specific roll number dhundna

---

# Algorithm for Searching

1. Start from head
2. Compare data
3. If found → success
4. Else move next

---

# C Program for Searching

```c
void search()
{
    struct node *temp;
    int item,found=0;

    temp=head;

    printf("Enter Element:");
    scanf("%d",&item);

    while(temp!=NULL)
    {
        if(temp->data==item)
        {
            found=1;
            break;
        }

        temp=temp->next;
    }

    if(found==1)
    {
        printf("Element Found");
    }
    else
    {
        printf("Element Not Found");
    }
}
```

---

# CIRCULAR LINKED LIST

# Introduction

Circular Linked List mein:
```text
Last node first node ko point karti hai
```

---

# Difference from Singly Linked List

Singly Linked List:
```text
Last node -> NULL
```

Circular Linked List:
```text
Last node -> HEAD
```

---

# Image Representation

```md
![Circular Linked List](images/circular-linked-list.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/d/df/Circularly-linked-list.svg

---

# Advantages of Circular Linked List

1. Continuous traversal possible
2. Better memory utilization
3. Queue implementation easy

---

# Applications

1. CPU scheduling
2. Multiplayer games
3. Circular queue

---

# Program to Create Circular Linked List

```c
#include<stdio.h>
#include<stdlib.h>

struct node
{
    int data;
    struct node *next;
};

struct node *head=NULL,*temp,*newnode;

void create()
{
    int choice=1;

    while(choice)
    {
        newnode=(struct node*)malloc(sizeof(struct node));

        printf("Enter Data:");
        scanf("%d",&newnode->data);

        if(head==NULL)
        {
            head=temp=newnode;
            newnode->next=head;
        }
        else
        {
            temp->next=newnode;
            temp=newnode;
            temp->next=head;
        }

        printf("Press 1 to continue:");
        scanf("%d",&choice);
    }
}
```

---

# DOUBLY LINKED LIST

# Introduction

Doubly Linked List mein:
```text
Har node:
- previous node ka address
- next node ka address
```

dono store karti hai.

---

# Structure

```text
PREV | DATA | NEXT
```

---

# Image Representation

```md
![Doubly Linked List](images/doubly-linked-list.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/5/5e/Doubly-linked-list.svg

---

# Example

```text
NULL <- 10 <-> 20 <-> 30 -> NULL
```

---

# Advantages of Doubly Linked List

1. Forward traversal
2. Backward traversal
3. Easy deletion

---

# Disadvantages

1. Extra memory required
2. Complex implementation

---

# Structure of Doubly Linked List Node

```c
struct node
{
    int data;
    struct node *prev;
    struct node *next;
};
```

---

# Program for Doubly Linked List

```c
#include<stdio.h>
#include<stdlib.h>

struct node
{
    int data;
    struct node *prev;
    struct node *next;
};

struct node *head=NULL,*newnode,*temp;

void create()
{
    int choice=1;

    while(choice)
    {
        newnode=(struct node*)malloc(sizeof(struct node));

        printf("Enter Data:");
        scanf("%d",&newnode->data);

        newnode->prev=NULL;
        newnode->next=NULL;

        if(head==NULL)
        {
            head=temp=newnode;
        }
        else
        {
            temp->next=newnode;
            newnode->prev=temp;
            temp=newnode;
        }

        printf("Press 1 to continue:");
        scanf("%d",&choice);
    }
}
```

---

# Applications of Linked List

Linked List:
```text
Real-world programming
```
mein extensively use hoti hai.

---

# Main Applications

1. Music Playlist
2. Browser Navigation
3. Image Viewer
4. Memory Management
5. Undo/Redo
6. Polynomial Representation
7. Graph Representation

---

# Music Playlist Example

Songs:
```text
Linked list ki tarah connected
```
hote hain.

Next aur previous song:
```text
Traversal
```
jaisa work karta hai.

---

# Browser Navigation

Browser:
- previous pages
- next pages

doubly linked list se manage karta hai.

---

# Memory Management

Operating systems:
```text
Free memory blocks
```
manage karne ke liye linked list use karte hain.

---

# Advantages of Linked List Over Array

| Linked List | Array |
|---|---|
| Dynamic size | Fixed size |
| Easy insertion | Difficult insertion |
| Easy deletion | Difficult deletion |
| More memory usage | Less memory usage |

---

# Important Points to Remember

- Linked list dynamic data structure hai.
- Node mein data aur pointer hota hai.
- Singly linked list one-way traversal karti hai.
- Circular linked list mein last node head ko point karti hai.
- Doubly linked list both direction traversal allow karti hai.
- Linked list insertion aur deletion easy banati hai.
- Searching sequentially hoti hai.

---

# Conclusion

Linked List ek powerful dynamic data structure hai jo:
- flexible memory allocation
- easy insertion
- easy deletion

provide karti hai.

Singly, Circular aur Doubly Linked Lists different applications ke liye use hoti hain. Operating systems, browsers, playlists aur memory management mein linked lists ka bahut important role hota hai.
