# DATA STRUCTURES AND ALGORITHMS

# UNIT – TREES AND GRAPHS

---

# TREES

# Introduction to Trees

Tree:
```text
Non-Linear Data Structure
```
hai jisme data:
```text
Hierarchical form
```
mein store hota hai.

Array aur Linked List:
- linear structures hain

Lekin tree:
```text
Parent-child relationship
```
follow karta hai.

---

# Real Life Example of Tree

Examples:
- Family tree
- Company hierarchy
- Folder structure
- School management system

---

# Example

```text
Principal
   |
Teachers
   |
Students
```

Ye hierarchical structure:
```text
Tree
```
jaisa hota hai.

---

# Tree Representation

```md
![Tree Structure](images/tree-structure.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/f/f7/Binary_tree.svg

---

# Basic Terminology of Tree

1. Root Node
2. Parent Node
3. Child Node
4. Leaf Node
5. Sibling
6. Degree
7. Level
8. Height

---

# Root Node

Tree ka:
```text
Topmost node
```
root node kehlata hai.

---

# Parent Node

Jo node:
```text
Dusri node ko connect karti hai
```
vo parent node hoti hai.

---

# Child Node

Jo node:
```text
Parent se connected hoti hai
```
vo child node hoti hai.

---

# Leaf Node

Jis node ka:
```text
Koi child nahi hota
```
use leaf node kehte hain.

---

# Sibling Nodes

Same parent wali nodes:
```text
Sibling
```
kehlati hain.

---

# Degree of Node

Node ke total children:
```text
Degree
```
kehlate hain.

---

# Height of Tree

Root se deepest node tak distance:
```text
Height
```
kehlata hai.

---

# Example Tree

```text
        A
       / \
      B   C
     / \
    D   E
```

---

# Identification

| Node | Type |
|---|---|
| A | Root |
| B,C | Child |
| D,E | Leaf |

---

# Tree Representation Using Linked List

# Introduction

Tree ko memory mein:
```text
Linked List
```
ke through represent kiya jata hai.

Har node:
- data
- left pointer
- right pointer

store karti hai.

---

# Structure of Tree Node

```c
struct node
{
    int data;
    struct node *left;
    struct node *right;
};
```

---

# Why Linked Representation Used

Advantages:
1. Dynamic memory allocation
2. Better flexibility
3. Easy insertion/deletion

---

# Binary Tree

# Introduction

Binary Tree:
```text
Special tree
```
hai jisme:
```text
Har node maximum 2 children
```
rakh sakti hai.

Children:
1. Left Child
2. Right Child

---

# Example of Binary Tree

```text
        10
       /  \
      20   30
     / \
    40 50
```

---

# Image Representation

```md
![Binary Tree](images/binary-tree.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/f/f7/Binary_tree.svg

---

# Types of Binary Tree

1. Full Binary Tree
2. Complete Binary Tree
3. Perfect Binary Tree
4. Skewed Binary Tree

---

# Full Binary Tree

Har node:
```text
0 ya 2 children
```
rakhti hai.

---

# Complete Binary Tree

Saare levels:
```text
Completely filled
```
hote hain except last.

---

# Perfect Binary Tree

Sab leaf nodes:
```text
Same level par
```
hote hain.

---

# Linear Representation of Binary Tree

# Introduction

Binary tree ko:
```text
Array
```
mein bhi represent kar sakte hain.

---

# Formula

Suppose:
Parent index = i

Then:
```text
Left Child = 2i
Right Child = 2i+1
```

---

# Example

| Index | Value |
|---|---|
| 1 | A |
| 2 | B |
| 3 | C |
| 4 | D |

---

# Advantages

1. Fast access
2. Simple implementation

---

# Disadvantages

1. Memory wastage
2. Fixed size

---

# Linked Representation of Binary Tree

# Introduction

Binary tree ka most common representation:
```text
Linked Representation
```
hai.

---

# Structure

Har node:
- data
- left pointer
- right pointer

store karti hai.

---

# C Structure

```c
struct node
{
    int data;
    struct node *left;
    struct node *right;
};
```

---

# Advantages

1. Dynamic size
2. No memory wastage
3. Flexible structure

---

# Creating Binary Tree Node

# Program

```c
#include<stdio.h>
#include<stdlib.h>

struct node
{
    int data;
    struct node *left;
    struct node *right;
};

struct node* createNode(int value)
{
    struct node *newnode;

    newnode=(struct node*)malloc(sizeof(struct node));

    newnode->data=value;
    newnode->left=NULL;
    newnode->right=NULL;

    return newnode;
}
```

---

# Tree Traversal

# Introduction

Tree ke nodes ko systematic order mein visit karna:
```text
Traversal
```
kehlata hai.

---

# Types of Traversal

1. Inorder Traversal
2. Preorder Traversal
3. Postorder Traversal

---

# Example Tree

```text
        A
       / \
      B   C
     / \
    D   E
```

---

# Inorder Traversal

# Rule

```text
LEFT -> ROOT -> RIGHT
```

---

# Example

```text
D B E A C
```

---

# C Program for Inorder Traversal

```c
void inorder(struct node *root)
{
    if(root!=NULL)
    {
        inorder(root->left);

        printf("%d ",root->data);

        inorder(root->right);
    }
}
```

---

# Preorder Traversal

# Rule

```text
ROOT -> LEFT -> RIGHT
```

---

# Example

```text
A B D E C
```

---

# C Program for Preorder Traversal

```c
void preorder(struct node *root)
{
    if(root!=NULL)
    {
        printf("%d ",root->data);

        preorder(root->left);

        preorder(root->right);
    }
}
```

---

# Postorder Traversal

# Rule

```text
LEFT -> RIGHT -> ROOT
```

---

# Example

```text
D E B C A
```

---

# C Program for Postorder Traversal

```c
void postorder(struct node *root)
{
    if(root!=NULL)
    {
        postorder(root->left);

        postorder(root->right);

        printf("%d ",root->data);
    }
}
```

---

# Complete Binary Tree Traversal Program

```c
#include<stdio.h>
#include<stdlib.h>

struct node
{
    int data;
    struct node *left;
    struct node *right;
};

struct node* createNode(int value)
{
    struct node *newnode;

    newnode=(struct node*)malloc(sizeof(struct node));

    newnode->data=value;
    newnode->left=NULL;
    newnode->right=NULL;

    return newnode;
}

void inorder(struct node *root)
{
    if(root!=NULL)
    {
        inorder(root->left);
        printf("%d ",root->data);
        inorder(root->right);
    }
}

void preorder(struct node *root)
{
    if(root!=NULL)
    {
        printf("%d ",root->data);
        preorder(root->left);
        preorder(root->right);
    }
}

void postorder(struct node *root)
{
    if(root!=NULL)
    {
        postorder(root->left);
        postorder(root->right);
        printf("%d ",root->data);
    }
}

void main()
{
    struct node *root;

    root=createNode(10);

    root->left=createNode(20);
    root->right=createNode(30);

    root->left->left=createNode(40);
    root->left->right=createNode(50);

    printf("Inorder Traversal:\n");
    inorder(root);

    printf("\nPreorder Traversal:\n");
    preorder(root);

    printf("\nPostorder Traversal:\n");
    postorder(root);
}
```

---

# Output

```text
Inorder Traversal:
40 20 50 10 30

Preorder Traversal:
10 20 40 50 30

Postorder Traversal:
40 50 20 30 10
```

---

# Applications of Trees

1. File systems
2. Database indexing
3. Compiler design
4. Decision trees
5. AI systems
6. XML/HTML structure

---

# GRAPHS

# Introduction to Graph

Graph:
```text
Non-linear data structure
```
hai jisme:
- nodes
- edges

hote hain.

---

# Components of Graph

1. Vertex (Node)
2. Edge

---

# Real Life Example

Examples:
- Google Maps
- Social Networks
- Railway routes
- Facebook friends

---

# Graph Representation

```md
![Graph Representation](images/graph-representation.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/5/5b/6n-graf.svg

---

# Terminology of Graph

1. Vertex
2. Edge
3. Adjacent Vertex
4. Path
5. Cycle

---

# Vertex

Graph ka node:
```text
Vertex
```
kehlata hai.

---

# Edge

Vertices ko connect karne wali line:
```text
Edge
```
kehlati hai.

---

# Types of Graph

1. Directed Graph
2. Undirected Graph

---

# Directed Graph

Edges direction show karti hain.

---

# Undirected Graph

Edges direction show nahi karti.

---

# Graph Representation Methods

1. Adjacency Matrix
2. Adjacency List

---

# Adjacency Matrix

# Introduction

Graph ko:
```text
2D Array
```
mein represent karna:
```text
Adjacency Matrix
```
kehlata hai.

---

# Example Graph

```text
A -- B
|    |
C -- D
```

---

# Adjacency Matrix Table

|   | A | B | C | D |
|---|---|---|---|---|
| A | 0 | 1 | 1 | 0 |
| B | 1 | 0 | 0 | 1 |
| C | 1 | 0 | 0 | 1 |
| D | 0 | 1 | 1 | 0 |

---

# Advantages

1. Simple implementation
2. Fast edge checking

---

# Disadvantages

1. Memory wastage
2. Large graphs difficult

---

# C Program for Adjacency Matrix

```c
#include<stdio.h>

void main()
{
    int graph[4][4]={
        {0,1,1,0},
        {1,0,0,1},
        {1,0,0,1},
        {0,1,1,0}
    };

    int i,j;

    printf("Adjacency Matrix:\n");

    for(i=0;i<4;i++)
    {
        for(j=0;j<4;j++)
        {
            printf("%d ",graph[i][j]);
        }

        printf("\n");
    }
}
```

---

# Graph Traversal

# Introduction

Graph ke nodes ko systematically visit karna:
```text
Traversal
```
kehlata hai.

---

# Types of Graph Traversal

1. Breadth First Search (BFS)
2. Depth First Search (DFS)

---

# Breadth First Search (BFS)

# Introduction

BFS:
```text
Level by level traversal
```
karta hai.

Queue:
```text
Use hoti hai
```

---

# Working of BFS

1. Start node visit
2. Adjacent nodes visit
3. Queue maintain

---

# Real Life Example

Social media friend suggestions:
```text
BFS concept
```
use karte hain.

---

# BFS Traversal Example

```text
A -> B -> C -> D
```

---

# C Program for BFS

```c
#include<stdio.h>

int graph[5][5],visited[5],queue[5];
int front=-1,rear=-1;

void bfs(int v,int n)
{
    int i;

    for(i=0;i<n;i++)
    {
        if(graph[v][i] && !visited[i])
        {
            queue[++rear]=i;
        }
    }

    if(front<=rear)
    {
        visited[queue[front]]=1;

        bfs(queue[front++],n);
    }
}

void main()
{
    int n=4,i,j;

    int g[4][4]={
        {0,1,1,0},
        {1,0,0,1},
        {1,0,0,1},
        {0,1,1,0}
    };

    for(i=0;i<n;i++)
    {
        for(j=0;j<n;j++)
        {
            graph[i][j]=g[i][j];
        }
    }

    printf("BFS Traversal:\n");

    visited[0]=1;

    printf("0 ");

    bfs(0,n);

    for(i=1;i<n;i++)
    {
        if(visited[i])
        {
            printf("%d ",i);
        }
    }
}
```

---

# Depth First Search (DFS)

# Introduction

DFS:
```text
Depth mein traversal
```
karta hai.

Stack ya recursion:
```text
Use hota hai
```

---

# Working of DFS

1. Start node visit
2. Deepest node tak jao
3. Backtracking karo

---

# Real Life Example

Maze solving:
```text
DFS
```
concept use karta hai.

---

# DFS Traversal Example

```text
A -> B -> D -> C
```

---

# C Program for DFS

```c
#include<stdio.h>

int graph[5][5],visited[5],n;

void dfs(int v)
{
    int i;

    visited[v]=1;

    printf("%d ",v);

    for(i=0;i<n;i++)
    {
        if(graph[v][i]==1 && visited[i]==0)
        {
            dfs(i);
        }
    }
}

void main()
{
    int i,j;

    n=4;

    int g[4][4]={
        {0,1,1,0},
        {1,0,0,1},
        {1,0,0,1},
        {0,1,1,0}
    };

    for(i=0;i<n;i++)
    {
        for(j=0;j<n;j++)
        {
            graph[i][j]=g[i][j];
        }
    }

    printf("DFS Traversal:\n");

    dfs(0);
}
```

---

# Difference Between BFS and DFS

| BFS | DFS |
|---|---|
| Queue use karta hai | Stack/Recursion use karta hai |
| Level-wise traversal | Depth-wise traversal |
| More memory | Less memory |
| Shortest path useful | Maze solving useful |

---

# Applications of Graphs

1. Google Maps
2. Social Networks
3. Networking
4. AI systems
5. Path finding
6. Recommendation systems

---

# Important Points to Remember

- Tree hierarchical structure hoti hai.
- Root topmost node hota hai.
- Binary tree max 2 children allow karti hai.
- Inorder = LEFT ROOT RIGHT
- Preorder = ROOT LEFT RIGHT
- Postorder = LEFT RIGHT ROOT
- Graph vertices aur edges se milkar banta hai.
- Adjacency matrix graph representation hai.
- BFS queue use karta hai.
- DFS recursion ya stack use karta hai.

---

# Conclusion

Trees aur Graphs:
```text
Advanced non-linear data structures
```
hain jo:
- hierarchical data
- network relationships

manage karne mein useful hote hain.

Binary trees searching aur hierarchical systems mein important role play karti hain. BFS aur DFS graph traversal techniques networking, AI aur path finding systems mein extensively use hoti hain.
