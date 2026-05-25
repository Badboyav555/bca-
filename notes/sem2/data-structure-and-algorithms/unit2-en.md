# DATA STRUCTURES AND ALGORITHMS – UNIT 2

# QUEUES IN DATA STRUCTURES USING C

---

# Introduction to Queue

A Queue is a linear data structure that follows:
```text
FIFO (First In First Out)
```

This means:
- The element inserted first is removed first.

Queue works exactly like a real-life waiting line.

---

# Real Life Example of Queue

Examples of queue:
- Ticket counter line
- ATM line
- School admission line
- Railway reservation queue

Suppose five people stand in ATM line.

The person who entered first:
- Leaves first

Similarly queue works in computer memory.

---

# Definition of Queue

A Queue is a linear data structure in which insertion takes place from the REAR end and deletion takes place from the FRONT end.

---

# Memory Representation of Queue

```md
![Queue Representation](images/queue-representation.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/5/52/Data_Queue.svg

---

# Basic Terminologies of Queue

| Term | Meaning |
|---|---|
| FRONT | Starting point of queue |
| REAR | Ending point of queue |
| ENQUEUE | Insertion operation |
| DEQUEUE | Deletion operation |

---

# Queue Operations

Main operations performed on queue:

1. Insertion (Enqueue)
2. Deletion (Dequeue)
3. Display
4. Peek

---

# ENQUEUE Operation

Enqueue means inserting element into queue from REAR side.

---

# DEQUEUE Operation

Dequeue means deleting element from FRONT side.

---

# PEEK Operation

Peek returns front element without deleting it.

---

# Characteristics of Queue

- FIFO structure
- Insertion at rear
- Deletion at front
- Sequential data processing

---

# Advantages of Queue

- Easy scheduling
- Efficient data management
- Useful in multitasking systems

---

# Disadvantages of Queue

- Fixed size in arrays
- Memory wastage possible
- Random access not possible

---

# Queue Overflow

Queue Overflow occurs when:
- Queue becomes full
- Further insertion attempted

---

# Queue Underflow

Queue Underflow occurs when:
- Queue becomes empty
- Deletion attempted

---

# Array Implementation of Queue

Queues can be implemented using:
- Arrays
- Linked Lists

Here we use arrays because they are simple and commonly asked in exams.

---

# Queue Representation Using Array

```md
![Queue Array Representation](images/queue-array.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/5/52/Data_Queue.svg

---

# Algorithm for ENQUEUE

```text
1. Check if queue is full
2. Increment REAR
3. Insert element at REAR
```

---

# Algorithm for DEQUEUE

```text
1. Check if queue is empty
2. Delete element from FRONT
3. Increment FRONT
```

---

# C Program for Queue Operations

```c
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>

#define SIZE 5

int queue[SIZE];
int front=-1;
int rear=-1;

void enqueue()
{
    int value;

    if(rear==SIZE-1)
    {
        printf("\nQueue Overflow");
    }
    else
    {
        if(front==-1)
        {
            front=0;
        }

        printf("\nEnter Value: ");
        scanf("%d",&value);

        rear++;

        queue[rear]=value;

        printf("\n%d Inserted",value);
    }
}

void dequeue()
{
    if(front==-1 || front>rear)
    {
        printf("\nQueue Underflow");
    }
    else
    {
        printf("\nDeleted Element: %d",queue[front]);

        front++;
    }
}

void peek()
{
    if(front==-1 || front>rear)
    {
        printf("\nQueue Empty");
    }
    else
    {
        printf("\nFront Element: %d",queue[front]);
    }
}

void display()
{
    int i;

    if(front==-1 || front>rear)
    {
        printf("\nQueue Empty");
    }
    else
    {
        printf("\nQueue Elements:\n");

        for(i=front;i<=rear;i++)
        {
            printf("%d ",queue[i]);
        }
    }
}

void main()
{
    int choice;

    clrscr();

    while(1)
    {
        printf("\n\n--- QUEUE MENU ---");
        printf("\n1.Enqueue");
        printf("\n2.Dequeue");
        printf("\n3.Peek");
        printf("\n4.Display");
        printf("\n5.Exit");

        printf("\nEnter Choice: ");
        scanf("%d",&choice);

        switch(choice)
        {
            case 1:
                enqueue();
                break;

            case 2:
                dequeue();
                break;

            case 3:
                peek();
                break;

            case 4:
                display();
                break;

            case 5:
                exit(0);

            default:
                printf("\nInvalid Choice");
        }
    }

    getch();
}
```

---

# Sample Output

```text
--- QUEUE MENU ---
1.Enqueue
2.Dequeue
3.Peek
4.Display
5.Exit

Enter Choice: 1
Enter Value: 10

10 Inserted
```

---

# Working of Queue

Suppose queue size is:
```text
5
```

Operations:

```text
Enqueue 10
Enqueue 20
Enqueue 30
```

Queue becomes:

```text
FRONT -> 10 20 30 <- REAR
```

After one dequeue:

```text
FRONT -> 20 30 <- REAR
```

---

# Problem in Simple Queue

Suppose queue size:
```text
5
```

After multiple deletions:
- Empty spaces appear at front

But insertion still cannot occur if rear reaches end.

This causes:
```text
Memory wastage
```

To solve this problem:
```text
Circular Queue is used
```

---

# CIRCULAR QUEUE

# Introduction to Circular Queue

Circular Queue is an improved version of simple queue where last position connects to first position.

It forms a circular structure.

---

# Memory Representation of Circular Queue

```md
![Circular Queue](images/circular-queue.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/2/29/Data_Circular_Queue.png

---

# Working of Circular Queue

In circular queue:
- Rear moves circularly
- Empty spaces are reused

---

# Advantages of Circular Queue

- Efficient memory utilization
- No wastage of space
- Faster operations

---

# Conditions in Circular Queue

---

# Queue Full Condition

```c
(front==0 && rear==SIZE-1) || (front==rear+1)
```

---

# Queue Empty Condition

```c
front==-1
```

---

# Algorithm for Circular Queue Insertion

```text
1. Check if queue full
2. If first insertion:
      front=rear=0
3. Else move rear circularly
4. Insert element
```

---

# Algorithm for Circular Queue Deletion

```text
1. Check if queue empty
2. Delete front element
3. Move front circularly
```

---

# C Program for Circular Queue

```c
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>

#define SIZE 5

int cq[SIZE];
int front=-1;
int rear=-1;

void enqueue()
{
    int value;

    if((front==0 && rear==SIZE-1) || (front==rear+1))
    {
        printf("\nCircular Queue Overflow");
    }
    else
    {
        printf("\nEnter Value: ");
        scanf("%d",&value);

        if(front==-1)
        {
            front=rear=0;
        }
        else if(rear==SIZE-1)
        {
            rear=0;
        }
        else
        {
            rear++;
        }

        cq[rear]=value;

        printf("\n%d Inserted",value);
    }
}

void dequeue()
{
    if(front==-1)
    {
        printf("\nCircular Queue Underflow");
    }
    else
    {
        printf("\nDeleted Element: %d",cq[front]);

        if(front==rear)
        {
            front=rear=-1;
        }
        else if(front==SIZE-1)
        {
            front=0;
        }
        else
        {
            front++;
        }
    }
}

void display()
{
    int i;

    if(front==-1)
    {
        printf("\nQueue Empty");
    }
    else
    {
        printf("\nQueue Elements:\n");

        if(front<=rear)
        {
            for(i=front;i<=rear;i++)
            {
                printf("%d ",cq[i]);
            }
        }
        else
        {
            for(i=front;i<SIZE;i++)
            {
                printf("%d ",cq[i]);
            }

            for(i=0;i<=rear;i++)
            {
                printf("%d ",cq[i]);
            }
        }
    }
}

void main()
{
    int choice;

    clrscr();

    while(1)
    {
        printf("\n\n--- CIRCULAR QUEUE MENU ---");
        printf("\n1.Enqueue");
        printf("\n2.Dequeue");
        printf("\n3.Display");
        printf("\n4.Exit");

        printf("\nEnter Choice: ");
        scanf("%d",&choice);

        switch(choice)
        {
            case 1:
                enqueue();
                break;

            case 2:
                dequeue();
                break;

            case 3:
                display();
                break;

            case 4:
                exit(0);

            default:
                printf("\nInvalid Choice");
        }
    }

    getch();
}
```

---

# Difference Between Simple Queue and Circular Queue

| Simple Queue | Circular Queue |
|---|---|
| Memory wastage possible | Efficient memory usage |
| Rear cannot reuse space | Rear reuses free space |
| Linear structure | Circular structure |

---

# Applications of Queue

Queues are widely used in computer science and real-life systems.

---

# 1. CPU Scheduling

Operating systems use queue for:
- Process scheduling
- Task management

---

# 2. Printer Queue

Print requests are stored in queue.

First print request:
- Executes first

---

# 3. Keyboard Buffer

Characters typed by user are stored in queue.

---

# 4. Ticket Booking System

Railway and movie ticket systems use queues.

---

# 5. BFS Traversal

Queues are used in:
- Graph algorithms
- Tree traversal

---

# 6. Call Center Systems

Customer calls are processed using queue.

---

# Real Life Example of Queue Application

Suppose:
100 users send print commands.

Printer handles them one-by-one using queue.

---

# Time Complexity of Queue Operations

| Operation | Complexity |
|---|---|
| Enqueue | O(1) |
| Dequeue | O(1) |
| Peek | O(1) |

---

# Important Points to Remember

- Queue follows FIFO principle.
- Insertion occurs at rear.
- Deletion occurs at front.
- Enqueue inserts element.
- Dequeue deletes element.
- Queue Overflow occurs when full.
- Queue Underflow occurs when empty.
- Circular queue removes memory wastage.
- Circular queue uses circular structure.
- Queues are used in scheduling and buffering.

---

# Conclusion

Queue is an important linear data structure used for sequential processing of data. It follows FIFO principle where first inserted element is removed first.

Queues are widely used in operating systems, printers, call centers, ticket booking systems, and process scheduling. Circular queues improve memory utilization by reusing empty spaces efficiently.

Understanding queues is essential because they form the foundation of advanced data structures and real-world computing systems.
