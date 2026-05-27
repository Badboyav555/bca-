# DATA STRUCTURES AND ALGORITHMS

# UNIT – SEARCHING, SORTING AND HASHING

---

# Introduction to Searching and Sorting

Computer science mein:
```text
Searching aur Sorting
```
bahut important concepts hain.

Large amount of data ko:
- arrange
- search
- manage

karne ke liye ye techniques use hoti hain.

---

# Real Life Example

Suppose:
- school mein 500 students ke records hain

Agar records:
```text
Sorted
```
hain:
- student easily find hoga

Agar random order mein hain:
- searching difficult hogi

Isi liye:
```text
Searching aur Sorting
```
important hain.

---

# SEARCHING

# Introduction to Searching

Data structure mein:
```text
Specific element find karna
```
searching kehlata hai.

---

# Types of Searching

1. Sequential Searching
2. Binary Searching

---

# SEQUENTIAL SEARCHING

# Introduction

Sequential Search:
```text
Linear Search
```
bhi kehlati hai.

Isme:
```text
Elements ek-ek karke check hote hain
```

---

# Working of Sequential Search

1. First element check
2. Match na mile toh next check
3. Last tak continue

---

# Real Life Example

Suppose:
- notebook mein student name dhundna

Aap:
```text
Page by page search
```
karte ho.

Ye:
```text
Sequential Searching
```
jaisa hai.

---

# Example

Array:
```text
10 20 30 40 50
```

Search:
```text
30
```

Steps:
- 10 check
- 20 check
- 30 found

---

# Advantages

1. Simple implementation
2. No sorting needed
3. Small data ke liye useful

---

# Disadvantages

1. Slow for large data
2. More comparisons

---

# C Program for Sequential Search

```c
#include<stdio.h>

void main()
{
    int arr[5]={10,20,30,40,50};
    int i,item,found=0;

    printf("Enter element to search:");
    scanf("%d",&item);

    for(i=0;i<5;i++)
    {
        if(arr[i]==item)
        {
            found=1;
            break;
        }
    }

    if(found==1)
    {
        printf("Element Found at position %d",i+1);
    }
    else
    {
        printf("Element Not Found");
    }
}
```

---

# Output

```text
Enter element to search:30

Element Found at position 3
```

---

# BINARY SEARCHING

# Introduction

Binary Search:
```text
Fast searching technique
```
hai.

Condition:
```text
Array sorted honi chahiye
```

---

# Working of Binary Search

1. Middle element check
2. Agar smaller:
   - left side search
3. Agar greater:
   - right side search

---

# Real Life Example

Dictionary mein word search:
```text
Binary Search
```
jaisa hota hai.

Aap:
- directly middle pages open karte ho

---

# Example

Array:
```text
10 20 30 40 50
```

Search:
```text
40
```

Middle:
```text
30
```

40 > 30:
- right side search

Then:
```text
40 found
```

---

# Advantages

1. Fast searching
2. Less comparisons
3. Efficient for large data

---

# Disadvantages

1. Sorted data needed
2. Complex than linear search

---

# C Program for Binary Search

```c
#include<stdio.h>

void main()
{
    int arr[5]={10,20,30,40,50};

    int low=0,high=4,mid,item;

    printf("Enter element:");
    scanf("%d",&item);

    while(low<=high)
    {
        mid=(low+high)/2;

        if(arr[mid]==item)
        {
            printf("Element Found at position %d",mid+1);
            break;
        }
        else if(arr[mid]<item)
        {
            low=mid+1;
        }
        else
        {
            high=mid-1;
        }
    }

    if(low>high)
    {
        printf("Element Not Found");
    }
}
```

---

# Output

```text
Enter element:40

Element Found at position 4
```

---

# Difference Between Sequential and Binary Search

| Sequential Search | Binary Search |
|---|---|
| Slow | Fast |
| No sorting needed | Sorted array needed |
| Simple | More complex |
| Large data inefficient | Large data efficient |

---

# SORTING

# Introduction to Sorting

Data ko:
```text
Ascending ya Descending order
```
mein arrange karna:
```text
Sorting
```
kehlata hai.

---

# Example

Unsorted:
```text
50 20 10 40
```

Sorted:
```text
10 20 40 50
```

---

# Types of Sorting

1. Bubble Sort
2. Selection Sort
3. Insertion Sort
4. Quick Sort
5. Merge Sort

---

# BUBBLE SORT

# Introduction

Bubble Sort:
```text
Adjacent elements compare
```
karta hai.

Bigger element:
```text
End ki taraf move hota hai
```

---

# Real Life Example

Water bubbles:
```text
Upper side move karti hain
```

Isi liye:
```text
Bubble Sort
```
naam pada.

---

# Working

Array:
```text
50 20 10 40
```

Pass 1:
```text
20 10 40 50
```

---

# Advantages

1. Simple
2. Easy to understand

---

# Disadvantages

1. Slow
2. Large data inefficient

---

# C Program for Bubble Sort

```c
#include<stdio.h>

void main()
{
    int arr[5]={50,20,10,40,30};

    int i,j,temp;

    for(i=0;i<5;i++)
    {
        for(j=0;j<4-i;j++)
        {
            if(arr[j]>arr[j+1])
            {
                temp=arr[j];
                arr[j]=arr[j+1];
                arr[j+1]=temp;
            }
        }
    }

    printf("Sorted Array:\n");

    for(i=0;i<5;i++)
    {
        printf("%d ",arr[i]);
    }
}
```

---

# Output

```text
Sorted Array:
10 20 30 40 50
```

---

# SELECTION SORT

# Introduction

Selection Sort:
```text
Minimum element select
```
karta hai aur correct position par place karta hai.

---

# Working

1. Smallest element find
2. First position swap
3. Repeat process

---

# Advantages

1. Less swaps
2. Simple logic

---

# Disadvantages

1. Slow for large data

---

# C Program for Selection Sort

```c
#include<stdio.h>

void main()
{
    int arr[5]={64,25,12,22,11};

    int i,j,min,temp;

    for(i=0;i<4;i++)
    {
        min=i;

        for(j=i+1;j<5;j++)
        {
            if(arr[j]<arr[min])
            {
                min=j;
            }
        }

        temp=arr[i];
        arr[i]=arr[min];
        arr[min]=temp;
    }

    printf("Sorted Array:\n");

    for(i=0;i<5;i++)
    {
        printf("%d ",arr[i]);
    }
}
```

---

# INSERTION SORT

# Introduction

Insertion Sort:
```text
Cards arranging
```
jaisa work karta hai.

---

# Real Life Example

Playing cards:
- ek-ek card correct position par insert karte ho

---

# Working

1. One element pick
2. Correct position insert

---

# Advantages

1. Small data efficient
2. Stable sorting

---

# Disadvantages

1. Large data slow

---

# C Program for Insertion Sort

```c
#include<stdio.h>

void main()
{
    int arr[5]={12,11,13,5,6};

    int i,key,j;

    for(i=1;i<5;i++)
    {
        key=arr[i];

        j=i-1;

        while(j>=0 && arr[j]>key)
        {
            arr[j+1]=arr[j];
            j--;
        }

        arr[j+1]=key;
    }

    printf("Sorted Array:\n");

    for(i=0;i<5;i++)
    {
        printf("%d ",arr[i]);
    }
}
```

---

# QUICK SORT

# Introduction

Quick Sort:
```text
Fast divide and conquer algorithm
```
hai.

---

# Working

1. Pivot select
2. Smaller left
3. Greater right
4. Recursively sort

---

# Advantages

1. Very fast
2. Efficient for large data

---

# Disadvantages

1. Complex implementation

---

# C Program for Quick Sort

```c
#include<stdio.h>

int partition(int arr[],int low,int high)
{
    int pivot=arr[high];

    int i=low-1,j,temp;

    for(j=low;j<high;j++)
    {
        if(arr[j]<pivot)
        {
            i++;

            temp=arr[i];
            arr[i]=arr[j];
            arr[j]=temp;
        }
    }

    temp=arr[i+1];
    arr[i+1]=arr[high];
    arr[high]=temp;

    return i+1;
}

void quicksort(int arr[],int low,int high)
{
    int pi;

    if(low<high)
    {
        pi=partition(arr,low,high);

        quicksort(arr,low,pi-1);

        quicksort(arr,pi+1,high);
    }
}

void main()
{
    int arr[5]={10,7,8,9,1};

    int i;

    quicksort(arr,0,4);

    printf("Sorted Array:\n");

    for(i=0;i<5;i++)
    {
        printf("%d ",arr[i]);
    }
}
```

---

# MERGE SORT

# Introduction

Merge Sort:
```text
Divide and Conquer
```
technique use karta hai.

---

# Working

1. Array divide
2. Recursively sort
3. Merge sorted arrays

---

# Advantages

1. Stable sorting
2. Large data efficient

---

# Disadvantages

1. Extra memory required

---

# Merge Sort Representation

```md
![Merge Sort](images/merge-sort.png)
```

Suggested Image Link:
https://upload.wikimedia.org/wikipedia/commons/c/cc/Merge-sort-example-300px.gif

---

# HASHING

# Introduction

Hashing:
```text
Fast data searching technique
```
hai.

---

# Working of Hashing

Data:
```text
Hash Function
```
through:
```text
Hash Table
```
mein convert hota hai.

---

# Real Life Example

Library:
- book number se directly shelf locate karna

Ye:
```text
Hashing
```
jaisa hai.

---

# Components of Hashing

1. Hash Function
2. Hash Table
3. Key

---

# Hash Function

Key ko:
```text
Index
```
mein convert karta hai.

---

# Example

```text
Index = Key % Size
```

---

# Example

Key:
```text
25
```

Size:
```text
10
```

Hash:
```text
25 % 10 = 5
```

---

# Advantages of Hashing

1. Very fast searching
2. Efficient data retrieval
3. Direct access

---

# Disadvantages

1. Collision problem
2. Extra memory needed

---

# Collision

Jab:
```text
Different keys same index
```
generate karti hain.

---

# Collision Resolution Methods

1. Chaining
2. Linear Probing

---

# Applications of Hashing

1. Password systems
2. Database indexing
3. Search engines
4. Symbol tables
5. Caching

---

# Difference Between Sorting Algorithms

| Algorithm | Speed | Complexity |
|---|---|---|
| Bubble Sort | Slow | Easy |
| Selection Sort | Medium | Easy |
| Insertion Sort | Medium | Easy |
| Quick Sort | Fast | Complex |
| Merge Sort | Fast | Complex |

---

# Important Points to Remember

- Sequential search linear search hai.
- Binary search sorted array par work karta hai.
- Bubble sort adjacent swapping karta hai.
- Selection sort minimum element select karta hai.
- Insertion sort card arrangement jaisa hai.
- Quick sort pivot use karta hai.
- Merge sort divide and conquer use karta hai.
- Hashing fast searching technique hai.

---

# Conclusion

Searching aur Sorting:
```text
Data processing ke core concepts
```
hain.

Searching:
- data locate karne

ke liye use hoti hai.

Sorting:
- data organize karne

ke liye use hoti hai.

Hashing:
```text
Very fast searching
```
provide karti hai.

Modern systems:
- databases
- search engines
- operating systems
- AI applications

mein searching, sorting aur hashing ka bahut important role hota hai.
