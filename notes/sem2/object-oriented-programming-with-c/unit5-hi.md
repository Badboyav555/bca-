# OBJECT ORIENTED PROGRAMMING USING C++

# UNIT – VIRTUAL FUNCTIONS, FRIEND FUNCTIONS, FILE HANDLING, STREAMS, TEMPLATES AND EXCEPTION HANDLING

---

# Virtual Functions

# Introduction

Object Oriented Programming mein kabhi situation aisi hoti hai jahan:
- base class pointer
- derived class object

ko refer karta hai.

Aise case mein normally:
```text
Base class function call hota hai
```

Lekin agar hum chahte hain:
```text
Runtime par actual object ke according function call ho
```

toh:
```text
Virtual Function
```
use karte hain.

---

# Simple Meaning

Virtual function:
```text
Run time polymorphism provide karta hai
```

---

# Real Life Example

Suppose:
```text
Animal
```
ek base class hai.

Animals:
- Dog
- Cat
- Cow

sabki:
```text
sound()
```
different hoti hai.

Agar hum runtime par decide karna chahein ki:
- Dog bark kare
- Cat meow kare

toh virtual function useful hota hai.

---

# Syntax

```cpp
virtual return_type function_name()
{
}
```

---

# Program Example

```cpp
#include<iostream.h>
#include<conio.h>

class Animal
{
    public:

    virtual void sound()
    {
        cout<<"Animal Sound";
    }
};

class Dog : public Animal
{
    public:

    void sound()
    {
        cout<<"Dog Barks";
    }
};

void main()
{
    Animal *a;

    Dog d;

    a=&d;

    clrscr();

    a->sound();

    getch();
}
```

---

# Output

```text
Dog Barks
```

---

# How Virtual Function Works

Compiler:
- late binding
- dynamic binding

use karta hai.

Function call runtime par decide hota hai.

---

# Advantages of Virtual Functions

1. Runtime polymorphism
2. Flexibility
3. Better extensibility
4. Real world behavior simulation

---

# Pure Virtual Function

# Introduction

Kabhi base class sirf interface provide karti hai.

Actual implementation derived class deti hai.

Aise function:
```text
Pure Virtual Function
```
kehlate hain.

---

# Syntax

```cpp
virtual void show()=0;
```

---

# Abstract Class

Jis class mein pure virtual function hota hai:
```text
Abstract Class
```
kehlati hai.

---

# Real Life Example

Suppose:
```text
Shape
```
sirf concept hai.

Actual shapes:
- Circle
- Rectangle
- Triangle

hote hain.

---

# Program Example

```cpp
#include<iostream.h>
#include<conio.h>

class Shape
{
    public:

    virtual void draw()=0;
};

class Circle : public Shape
{
    public:

    void draw()
    {
        cout<<"Drawing Circle";
    }
};

void main()
{
    Circle c;

    clrscr();

    c.draw();

    getch();
}
```

---

# Output

```text
Drawing Circle
```

---

# Friend Function

# Introduction

Normally:
- private members outside class access nahi hote.

Lekin kabhi external function ko private data access karwana hota hai.

Iske liye:
```text
Friend Function
```
use hota hai.

---

# Simple Meaning

Friend function:
```text
Class ka dost hota hai
```

Isliye:
- private data access kar sakta hai.

---

# Real Life Example

Suppose:
- Bank locker private hai
- Sirf trusted friend ko permission di gayi hai

Waise hi friend function:
- special access leta hai.

---

# Syntax

```cpp
friend return_type function_name();
```

---

# Program Example

```cpp
#include<iostream.h>
#include<conio.h>

class Demo
{
    int x;

    public:

    Demo()
    {
        x=100;
    }

    friend void show(Demo);
};

void show(Demo d)
{
    cout<<"Value = "<<d.x;
}

void main()
{
    Demo d;

    clrscr();

    show(d);

    getch();
}
```

---

# Output

```text
Value = 100
```

---

# Properties of Friend Function

- Class member nahi hota
- Object se call nahi hota
- Private members access kar sakta hai

---

# Advantages of Friend Function

1. Flexible access
2. Operator overloading useful
3. External processing possible

---

# File Handling

# Introduction

Program terminate hone ke baad normally data:
```text
Destroy ho jata hai
```

Permanent storage ke liye:
```text
File Handling
```
use hota hai.

---

# What is File?

File:
```text
Data storage ka medium
```
hoti hai.

---

# Real Life Example

Suppose school register:
- student data permanently store karta hai

Waise hi computer mein file:
- permanent data store karti hai.

---

# Advantages of File Handling

1. Permanent storage
2. Large data management
3. Easy retrieval
4. Data sharing

---

# Types of Files

1. Text File
2. Binary File

---

# Text File

Human readable hoti hai.

Example:
```text
.txt
```

---

# Binary File

Machine readable hoti hai.

Fast processing deti hai.

---

# File Streams

C++ mein file handling streams ke through hoti hai.

---

# Main File Stream Classes

1. ifstream
2. ofstream
3. fstream

---

# ifstream

File read karta hai.

---

# ofstream

File write karta hai.

---

# fstream

Read aur write dono karta hai.

---

# File Opening

```cpp
file.open("filename");
```

---

# File Closing

```cpp
file.close();
```

---

# Program to Write into File

```cpp
#include<iostream.h>
#include<conio.h>
#include<fstream.h>

void main()
{
    ofstream fout;

    clrscr();

    fout.open("student.txt");

    fout<<"Hello Students";

    fout.close();

    cout<<"Data Written";

    getch();
}
```

---

# Output

```text
Data Written
```

---

# Program to Read from File

```cpp
#include<iostream.h>
#include<conio.h>
#include<fstream.h>

void main()
{
    ifstream fin;

    char data[50];

    clrscr();

    fin.open("student.txt");

    fin>>data;

    cout<<data;

    fin.close();

    getch();
}
```

---

# Output

```text
Hello
```

---

# File Operation Functions

# open()

File open karta hai.

---

# close()

File close karta hai.

---

# get()

Single character read karta hai.

---

# put()

Single character write karta hai.

---

# getline()

Complete line read karta hai.

---

# write()

Binary data write karta hai.

---

# read()

Binary data read karta hai.

---

# File Attributes

# ios::in

Reading mode.

---

# ios::out

Writing mode.

---

# ios::app

Append mode.

Data end mein add hota hai.

---

# ios::binary

Binary mode.

---

# Example

```cpp
fstream file;

file.open("abc.txt",ios::out);
```

---

# Streams in C++

# Introduction

Stream:
```text
Data flow
```
ko represent karta hai.

---

# Types of Streams

1. Input Stream
2. Output Stream

---

# Input Stream

Data:
```text
Input device → Program
```

Example:
```cpp
cin
```

---

# Output Stream

Data:
```text
Program → Output device
```

Example:
```cpp
cout
```

---

# Real Life Example

Suppose water pipe:
- water flow karta hai

Waise hi stream:
- data flow karta hai

---

# Standard Streams

| Stream | Purpose |
|---|---|
| cin | Input |
| cout | Output |
| cerr | Error |
| clog | Log |

---

# Templates

# Introduction

Template:
```text
Generic Programming
```
provide karta hai.

Ek hi function:
- different data types
par work kar sakta hai.

---

# Why Templates Needed

Suppose:
- int addition
- float addition
- double addition

ke liye alag functions banana pad raha hai.

Template:
```text
Single generic function
```
provide karta hai.

---

# Real Life Example

Suppose universal charger:
- different phones charge karta hai

Waise hi template:
- different data types handle karta hai.

---

# Function Template Syntax

```cpp
template<class T>
```

---

# Program Example

```cpp
#include<iostream.h>
#include<conio.h>

template<class T>

T add(T a,T b)
{
    return a+b;
}

void main()
{
    clrscr();

    cout<<"Integer Sum = "<<add(10,20);

    cout<<"\nFloat Sum = "<<add(2.5,3.5);

    getch();
}
```

---

# Output

```text
Integer Sum = 30
Float Sum = 6
```

---

# Class Template

# Introduction

Class bhi generic ban sakti hai.

---

# Program Example

```cpp
#include<iostream.h>
#include<conio.h>

template<class T>

class Demo
{
    T x;

    public:

    Demo(T a)
    {
        x=a;
    }

    void show()
    {
        cout<<"Value = "<<x;
    }
};

void main()
{
    clrscr();

    Demo<int> d1(10);

    Demo<float> d2(5.5);

    d1.show();

    cout<<"\n";

    d2.show();

    getch();
}
```

---

# Output

```text
Value = 10
Value = 5.5
```

---

# Exception Handling

# Introduction

Program execution ke time:
- errors
- abnormal conditions

aa sakte hain.

In errors ko properly handle karna:
```text
Exception Handling
```
kehlata hai.

---

# Real Life Example

Suppose bike chalate time:
- accident possibility hoti hai

Helmet safety provide karta hai.

Waise hi exception handling:
- program crash hone se bachati hai.

---

# Keywords in Exception Handling

1. try
2. throw
3. catch

---

# try Block

Risky code yahan likhte hain.

---

# throw

Exception generate karta hai.

---

# catch

Exception handle karta hai.

---

# Syntax

```cpp
try
{
}

throw value;

catch(type variable)
{
}
```

---

# Program Example

```cpp
#include<iostream.h>
#include<conio.h>

void main()
{
    int a,b,c;

    clrscr();

    cout<<"Enter Two Numbers: ";
    cin>>a>>b;

    try
    {
        if(b==0)
        {
            throw b;
        }

        c=a/b;

        cout<<"Division = "<<c;
    }

    catch(int x)
    {
        cout<<"Division by Zero Error";
    }

    getch();
}
```

---

# Output

```text
Enter Two Numbers: 10 0

Division by Zero Error
```

---

# Advantages of Exception Handling

1. Prevents program crash
2. Better error management
3. Cleaner code
4. Reliable software

---

# Important Points to Remember

- Virtual function runtime polymorphism deta hai.
- Pure virtual function abstract class banata hai.
- Friend function private data access karta hai.
- File handling permanent storage provide karta hai.
- Streams data flow represent karti hain.
- Templates generic programming provide karte hain.
- Exception handling runtime errors manage karti hai.

---

# Conclusion

Virtual functions, friend functions, file handling, templates aur exception handling C++ ke advanced aur powerful concepts hain. Ye programming ko:
- flexible
- reusable
- secure
- efficient

banate hain.

File handling permanent storage provide karti hai, templates generic programming ko possible banate hain aur exception handling software ko reliable banati hai.

Ye concepts modern software development, operating systems, game engines aur enterprise applications mein extensively use hote hain.
