# DATA STRUCTURES AND ALGORITHMS

# UNIT – QUEUES

---

# Introduction to Queue

Queue:
```text
Linear Data Structure
```
hai jo:
```text
FIFO
```
principle follow karti hai.

FIFO ka matlab:
```text
First In First Out
```

Jo element:
```text
Sabse pehle insert hota hai
```
vo:
```text
Sabse pehle delete hota hai
```

---

# Real Life Example of Queue

Real life examples:
- Railway ticket line
- Bank queue
- School canteen line
- Bus stop line

Jo person:
```text
Sabse pehle line mein aata hai
```
uska kaam:
```text
Sabse pehle hota hai
```

Isi tarah queue work karti hai.

---

# Queue Representation

```md
![Queue Representation](images/queue-representation.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/5/52/Data_Queue.svg

---

# Basic Terminology of Queue

1. FRONT
2. REAR
3. ENQUEUE
4. DEQUEUE
5. Overflow
6. Underflow

---

# FRONT

Queue ka first element:
```text
FRONT
```
kehlata hai.

Deletion:
```text
Front se hoti hai
```

---

# REAR

Queue ka last element:
```text
REAR
```
kehlata hai.

Insertion:
```text
Rear par hoti hai
```

---

# ENQUEUE Operation

Queue mein new element insert karna:
```text
ENQUEUE
```
kehlata hai.

---

# DEQUEUE Operation

Queue se element remove karna:
```text
DEQUEUE
```
kehlata hai.

---

# Overflow Condition

Queue full hone par:
```text
Insertion possible nahi hota
```

Isko:
```text
Queue Overflow
```
kehte hain.

---

# Underflow Condition

Queue empty hone par:
```text
Deletion possible nahi hota
```

Isko:
```text
Queue Underflow
```
kehte hain.

---

# Characteristics of Queue

1. FIFO principle
2. Insertion from rear
3. Deletion from front
4. Ordered processing

---

# Queue Operations

Main operations:
1. Insertion
2. Deletion
3. Display
4. Peek

---

# Queue Implementation

Queue implement ki ja sakti hai:
1. Array using
2. Linked List using

Yahan hum:
```text
Array implementation
```
samjhenge.

---

# Queue Using Array

# Declaration

```c
int queue[5];
```

---

# Variables Used

```c
front = -1
rear = -1
```

---

# Working of Queue

Initially:
```text
Queue empty hoti hai
```

Insertion:
- rear increase hota hai

Deletion:
- front increase hota hai

---

# Queue Operation Flow

Example:

Insert:
```text
10,20,30
```

Queue:
```text
10 20 30
```

Delete:
```text
10 remove
```

Remaining:
```text
20 30
```

---

# Algorithm for ENQUEUE

1. Check overflow
2. If queue empty:
   - set front=0
3. Increment rear
4. Insert element

---

# Algorithm for DEQUEUE

1. Check underflow
2. Remove front element
3. Increment front

---

# C Program for Queue Implementation

```c
#include<stdio.h>

#define MAX 5

int queue[MAX];
int front=-1;
int rear=-1;

void enqueue(int value)
{
    if(rear==MAX-1)
    {
        printf("Queue Overflow\n");
    }
    else
    {
        if(front==-1)
        {
            front=0;
        }

        rear++;
        queue[rear]=value;

        printf("Inserted %d\n",value);
    }
}

void dequeue()
{
    if(front==-1 || front>rear)
    {
        printf("Queue Underflow\n");
    }
    else
    {
        printf("Deleted %d\n",queue[front]);
        front++;
    }
}

void display()
{
    int i;

    if(front==-1 || front>rear)
    {
        printf("Queue Empty\n");
    }
    else
    {
        printf("Queue Elements:\n");

        for(i=front;i<=rear;i++)
        {
            printf("%d\n",queue[i]);
        }
    }
}

void main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    display();

    dequeue();

    display();
}
```

---

# Output

```text
Inserted 10
Inserted 20
Inserted 30

Queue Elements:
10
20
30

Deleted 10

Queue Elements:
20
30
```

---

# Queue Memory Representation

| Index | Value |
|---|---|
| 0 | 10 |
| 1 | 20 |
| 2 | 30 |

FRONT:
```text
0
```

REAR:
```text
2
```

---

# Problems in Simple Queue

Simple queue mein:
```text
Memory wastage
```
problem hoti hai.

---

# Example

Suppose:
Queue size = 5

Insert:
```text
10 20 30 40 50
```

Delete:
```text
10 20
```

Now:
- front move ho gaya
- rear last index par hai

New insertion:
```text
Possible nahi
```

Even though:
```text
Starting positions empty hain
```

Ye problem:
```text
Circular Queue
```
solve karti hai.

---

# Circular Queue

# Introduction

Circular Queue:
```text
Last position ko first position se connect
```
karti hai.

Queue circular form mein behave karti hai.

---

# Real Life Example

Clock:
- circular movement karti hai.

Circular queue bhi:
```text
Same concept
```
follow karti hai.

---

# Advantages of Circular Queue

1. Better memory utilization
2. No memory wastage
3. Efficient implementation

---

# Circular Queue Representation

```md
![Circular Queue](images/circular-queue.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/6/65/Circular_queue.png

---

# Condition for Circular Queue Full

```c
(rear+1)%MAX==front
```

---

# Condition for Empty Queue

```c
front==-1
```

---

# Algorithm for Circular Queue Insertion

1. Check full condition
2. If empty:
   - front=0
3. rear=(rear+1)%MAX
4. Insert element

---

# Algorithm for Circular Queue Deletion

1. Check empty condition
2. Remove front element
3. front=(front+1)%MAX

---

# C Program for Circular Queue

```c
#include<stdio.h>

#define MAX 5

int cqueue[MAX];
int front=-1;
int rear=-1;

void enqueue(int value)
{
    if((rear+1)%MAX==front)
    {
        printf("Queue Overflow\n");
    }
    else
    {
        if(front==-1)
        {
            front=0;
        }

        rear=(rear+1)%MAX;
        cqueue[rear]=value;

        printf("Inserted %d\n",value);
    }
}

void dequeue()
{
    if(front==-1)
    {
        printf("Queue Underflow\n");
    }
    else
    {
        printf("Deleted %d\n",cqueue[front]);

        if(front==rear)
        {
            front=-1;
            rear=-1;
        }
        else
        {
            front=(front+1)%MAX;
        }
    }
}

void display()
{
    int i;

    if(front==-1)
    {
        printf("Queue Empty\n");
    }
    else
    {
        printf("Queue Elements:\n");

        i=front;

        while(i!=rear)
        {
            printf("%d\n",cqueue[i]);
            i=(i+1)%MAX;
        }

        printf("%d\n",cqueue[rear]);
    }
}

void main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    display();

    dequeue();

    display();
}
```

---

# Output

```text
Inserted 10
Inserted 20
Inserted 30

Queue Elements:
10
20
30

Deleted 10

Queue Elements:
20
30
```

---

# Applications of Queue

Queue:
```text
Real-world systems
```
mein extensively use hoti hai.

---

# Main Applications

1. CPU Scheduling
2. Printer Queue
3. Ticket Booking
4. Call Center
5. BFS Traversal
6. Networking
7. Task Scheduling

---

# CPU Scheduling

Operating System:
```text
Processes ko queue mein maintain karta hai
```

---

# Printer Queue

Multiple print requests:
```text
Queue mein store hoti hain
```

Jo request:
```text
Pehle aati hai
```
vo:
```text
Pehle print hoti hai
```

---

# Ticket Booking Example

Railway reservation system:
```text
Queue
```
use karta hai.

---

# Call Center Example

Customer calls:
```text
Waiting queue
```
mein store hoti hain.

---

# BFS Traversal

Graphs aur trees mein:
```text
Breadth First Search
```
queue use karta hai.

---

# Advantages of Queue

1. Ordered processing
2. Efficient scheduling
3. Simple implementation
4. Useful in multitasking

---

# Disadvantages of Queue

1. Fixed size issue
2. Overflow possible
3. Memory wastage in simple queue

---

# Difference Between Stack and Queue

| Stack | Queue |
|---|---|
| LIFO | FIFO |
| Insert/Delete same end | Insert/Delete different ends |
| Push/Pop | Enqueue/Dequeue |
| Example: Plates | Example: Ticket line |

---

# Important Points to Remember

- Queue FIFO principle follow karti hai.
- Insertion rear par hoti hai.
- Deletion front se hoti hai.
- ENQUEUE insertion operation hai.
- DEQUEUE deletion operation hai.
- Overflow queue full hone par hota hai.
- Underflow queue empty hone par hota hai.
- Circular queue memory wastage avoid karti hai.
- Queue scheduling systems mein extensively use hoti hai.

---

# Conclusion

Queue ek important linear data structure hai jo:
```text
FIFO principle
```
follow karti hai.

Simple queue:
- insertion
- deletion

operations perform karti hai.

Circular queue:
```text
Memory wastage problem solve
```
karti hai.

Queues:
- operating systems
- networking
- scheduling
- ticket booking
- printer management

jaise real-world applications mein bahut important role play karti hain.
