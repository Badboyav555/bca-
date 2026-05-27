# DATA STRUCTURES AND ALGORITHMS

# UNIT – 1

# ARRAYS AND STACKS

---

# Introduction to Data Structures

Computer:
```text
Data ko organize aur manage
```
karne ke liye different techniques use karta hai.

In techniques ko:
```text
Data Structures
```
kehte hain.

---

# Why Data Structures Important

Agar data properly organized na ho:
- searching slow hogi
- memory waste hogi
- processing difficult hogi

Data structures:
- fast processing
- efficient storage
- easy manipulation

provide karti hain.

---

# Real Life Example

Suppose:
- school books randomly room mein padi hain

Toh:
- specific book dhundna difficult hoga.

Lekin agar:
- subject wise arrange ho

Toh:
- easily mil jayegi.

Isi tarah computer mein bhi:
```text
Data Structures
```
important hain.

---

# Types of Data Structures

1. Primitive Data Structures
2. Non-Primitive Data Structures

---

# Primitive Data Structures

Examples:
- int
- char
- float

---

# Non-Primitive Data Structures

Examples:
- Array
- Stack
- Queue
- Linked List
- Tree
- Graph

---

# ARRAY

# Introduction to Array

Array:
```text
Same data type ke multiple elements ko store karne ka structure
```
hota hai.

---

# Real Life Example

Suppose:
5 students ke marks store karne hain.

Without array:
```c
int m1,m2,m3,m4,m5;
```

With array:
```c
int marks[5];
```

---

# Advantages of Array

1. Easy storage
2. Fast access
3. Less code
4. Memory efficient

---

# Characteristics of Array

1. Same data type elements
2. Contiguous memory allocation
3. Fixed size
4. Indexed access

---

# Image Representation

```md
![Array Representation](images/array-representation.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/5/5a/Array_en.svg

---

# Declaration of Array

# Syntax

```c
datatype arrayname[size];
```

---

# Example

```c
int marks[5];
```

---

# Array Initialization

```c
int marks[5]={10,20,30,40,50};
```

---

# Accessing Array Elements

Indexing:
```text
0 se start hoti hai
```

---

# Example

```c
marks[0]
marks[1]
```

---

# C Program of Array

```c
#include<stdio.h>

void main()
{
    int marks[5]={10,20,30,40,50};
    int i;

    for(i=0;i<5;i++)
    {
        printf("%d\n",marks[i]);
    }
}
```

---

# Output

```text
10
20
30
40
50
```

---

# Working of Array

Memory mein:
```text
Continuous locations
```
allocate hoti hain.

---

# Example

| Index | Value |
|---|---|
| 0 | 10 |
| 1 | 20 |
| 2 | 30 |
| 3 | 40 |
| 4 | 50 |

---

# Advantages of Arrays

1. Fast element access
2. Easy traversal
3. Simple implementation

---

# Disadvantages of Arrays

1. Fixed size
2. Memory wastage possible
3. Insertion/deletion difficult

---

# STACK

# Introduction to Stack

Stack:
```text
Linear data structure
```
hai jo:
```text
LIFO
```
principle follow karta hai.

LIFO:
```text
Last In First Out
```

---

# Real Life Example of Stack

Examples:
- Plate stack
- Books stack
- Browser history

Jo item:
```text
Sabse last mein add hoti hai
```
vo:
```text
Sabse pehle remove hoti hai
```

---

# Stack Terminology

1. PUSH
2. POP
3. TOP
4. Overflow
5. Underflow

---

# PUSH Operation

Stack mein new element add karna:
```text
PUSH
```
kehlata hai.

---

# POP Operation

Stack se element remove karna:
```text
POP
```
kehlata hai.

---

# TOP

Stack ka topmost element.

---

# Overflow

Stack full hone par insertion attempt.

---

# Underflow

Empty stack se deletion attempt.

---

# Image Representation

```md
![Stack Representation](images/stack-representation.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/b/b4/Lifo_stack.png

---

# Stack Implementation Using Array

# Algorithm for PUSH

1. Check overflow
2. Increment TOP
3. Insert element

---

# Algorithm for POP

1. Check underflow
2. Return top element
3. Decrement TOP

---

# C Program for Stack

```c
#include<stdio.h>
#define MAX 5

int stack[MAX];
int top=-1;

void push(int value)
{
    if(top==MAX-1)
    {
        printf("Stack Overflow\n");
    }
    else
    {
        top++;
        stack[top]=value;
        printf("Inserted %d\n",value);
    }
}

void pop()
{
    if(top==-1)
    {
        printf("Stack Underflow\n");
    }
    else
    {
        printf("Deleted %d\n",stack[top]);
        top--;
    }
}

void display()
{
    int i;

    if(top==-1)
    {
        printf("Stack Empty\n");
    }
    else
    {
        for(i=top;i>=0;i--)
        {
            printf("%d\n",stack[i]);
        }
    }
}

void main()
{
    push(10);
    push(20);
    push(30);

    display();

    pop();

    display();
}
```

---

# Output

```text
Inserted 10
Inserted 20
Inserted 30

30
20
10

Deleted 30

20
10
```

---

# Applications of Stack

# Introduction

Stack real-world programming mein bahut useful hai.

---

# Main Applications

1. Function Calling
2. Expression Evaluation
3. Parenthesis Matching
4. Undo Operation
5. Browser History
6. Recursion

---

# Function Calling

Program:
```text
Function calls ko stack mein store karta hai
```

---

# Browser History Example

Browser:
- recently visited pages
- stack mein maintain karta hai

Back button:
```text
POP operation
```
jaisa work karta hai.

---

# Recursion

# Introduction

Jab function:
```text
Khud ko call karta hai
```
toh:
```text
Recursion
```
kehlata hai.

---

# Real Life Example

Suppose:
stairs descend kar rahe ho:
- ek step
- phir next
- phir next

Same pattern repeat hota hai.

---

# Recursive Function Example

Factorial:
```text
5! = 5×4×3×2×1
```

---

# C Program for Recursion

```c
#include<stdio.h>

int fact(int n)
{
    if(n==1)
    {
        return 1;
    }
    else
    {
        return n*fact(n-1);
    }
}

void main()
{
    int result;

    result=fact(5);

    printf("Factorial=%d",result);
}
```

---

# Output

```text
Factorial=120
```

---

# Expression Evaluation

# Introduction

Arithmetic expressions:
- stack ke through evaluate hoti hain.

---

# Types of Expressions

1. Infix
2. Prefix
3. Postfix

---

# Infix Expression

Operator:
```text
Operands ke beech mein hota hai
```

Example:
```text
A+B
```

---

# Prefix Expression

Operator:
```text
Operands se pehle hota hai
```

Example:
```text
+AB
```

---

# Postfix Expression

Operator:
```text
Operands ke baad hota hai
```

Example:
```text
AB+
```

---

# Difference Between Prefix, Infix and Postfix

| Type | Example |
|---|---|
| Infix | A+B |
| Prefix | +AB |
| Postfix | AB+ |

---

# Advantages of Postfix

1. No brackets needed
2. Easy evaluation
3. Fast computation

---

# Evaluation of Postfix Expression Using Stack

# Example

Expression:
```text
23*5+
```

Means:
```text
(2×3)+5
```

---

# Step-by-Step Evaluation

1. Push 2
2. Push 3
3. Multiply
4. Push result
5. Push 5
6. Add

Final Result:
```text
11
```

---

# Algorithm for Postfix Evaluation

1. Scan expression
2. Push operands
3. Apply operators
4. Push result
5. Final value = answer

---

# C Program for Postfix Evaluation

```c
#include<stdio.h>
#include<ctype.h>

int stack[20];
int top=-1;

void push(int x)
{
    stack[++top]=x;
}

int pop()
{
    return stack[top--];
}

void main()
{
    char exp[]="23*5+";
    int i,a,b,result;

    for(i=0;exp[i]!='\0';i++)
    {
        if(isdigit(exp[i]))
        {
            push(exp[i]-48);
        }
        else
        {
            a=pop();
            b=pop();

            switch(exp[i])
            {
                case '+':
                    push(b+a);
                    break;

                case '*':
                    push(b*a);
                    break;
            }
        }
    }

    result=pop();

    printf("Result=%d",result);
}
```

---

# Output

```text
Result=11
```

---

# Parenthesis Matching Using Stack

# Introduction

Compiler:
```text
Brackets matching check
```
karne ke liye stack use karta hai.

---

# Example

Correct:
```text
(a+b)
```

Incorrect:
```text
(a+b
```

---

# Working

1. Opening bracket → PUSH
2. Closing bracket → POP
3. Final stack empty → valid expression

---

# Real Life Example

Programming languages:
- C
- Java
- Python

sab:
```text
Parenthesis checking
```
ke liye stack use karte hain.

---

# C Program for Parenthesis Matching

```c
#include<stdio.h>

char stack[20];
int top=-1;

void push(char x)
{
    stack[++top]=x;
}

void pop()
{
    top--;
}

void main()
{
    char exp[20];
    int i;

    printf("Enter Expression:");
    scanf("%s",exp);

    for(i=0;exp[i]!='\0';i++)
    {
        if(exp[i]=='(')
        {
            push(exp[i]);
        }

        if(exp[i]==')')
        {
            pop();
        }
    }

    if(top==-1)
    {
        printf("Balanced Expression");
    }
    else
    {
        printf("Unbalanced Expression");
    }
}
```

---

# Output

```text
Enter Expression:(a+b)

Balanced Expression
```

---

# Advantages of Stack

1. Easy implementation
2. Fast insertion/deletion
3. Useful in recursion
4. Expression handling

---

# Disadvantages of Stack

1. Limited access
2. Fixed size in array implementation
3. Overflow possible

---

# Important Points to Remember

- Array same datatype elements store karta hai.
- Array indexing 0 se start hoti hai.
- Stack LIFO principle follow karta hai.
- PUSH insertion operation hai.
- POP deletion operation hai.
- Overflow stack full hone par hota hai.
- Underflow empty stack par hota hai.
- Prefix operator first hota hai.
- Postfix operator last hota hai.
- Stack recursion aur parenthesis matching mein use hota hai.

---

# Conclusion

Arrays aur stacks computer science ke basic aur important data structures hain. Arrays:
- fast data access
- simple storage

provide karte hain.

Stacks:
- LIFO principle
- function calling
- recursion
- expression evaluation
- parenthesis matching

mein extensively use hote hain.

Programming aur compiler design mein stacks ka bahut important role hota hai.
