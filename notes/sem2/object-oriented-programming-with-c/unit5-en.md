# UNIT 5 – Virtual Functions, Friend Functions, File Handling, Streams, Templates and Exception Handling in C++


# Introduction to Virtual Functions

Virtual functions are one of the most important concepts in Object Oriented Programming because they help achieve Runtime Polymorphism.

Runtime polymorphism means:
- Function call is decided during program execution
- Not during compilation

Virtual functions allow derived class functions to override base class functions properly.

---

# Why Virtual Functions are Needed

Suppose we have:
- Base class pointer
- Derived class object

Normally, base class function gets called.

But using virtual functions, derived class function gets called automatically.

This helps programs behave dynamically.

---

# Real Life Example

Suppose a remote control is used for different devices.

Same button:
- Changes channel in TV
- Changes temperature in AC
- Controls music in speaker

Behavior changes depending on actual object.

Similarly, virtual functions allow same function call to behave differently.

---

# Syntax of Virtual Function

```cpp
virtual return_type function_name()
{
}
```

---

# Example Program Without Virtual Function

```cpp
#include<iostream.h>
#include<conio.h>

class Base
{
    public:

    void show()
    {
        cout<<"Base Class";
    }
};

class Derived : public Base
{
    public:

    void show()
    {
        cout<<"Derived Class";
    }
};

void main()
{
    Base *ptr;

    Derived d;

    ptr=&d;

    ptr->show();

    getch();
}
```

---

# Output

```text
Base Class
```

---

# Explanation

Even though pointer points to derived object, base class function executes.

---

# Example Program With Virtual Function

```cpp
#include<iostream.h>
#include<conio.h>

class Base
{
    public:

    virtual void show()
    {
        cout<<"Base Class";
    }
};

class Derived : public Base
{
    public:

    void show()
    {
        cout<<"Derived Class";
    }
};

void main()
{
    Base *ptr;

    Derived d;

    ptr=&d;

    ptr->show();

    getch();
}
```

---

# Output

```text
Derived Class
```

---

# Explanation

Because `show()` is virtual, compiler decides function during runtime.

Derived class function executes.

---

# Advantages of Virtual Functions

- Supports runtime polymorphism
- Increases flexibility
- Makes programs dynamic
- Improves extensibility

---

# Pure Virtual Function

A virtual function with no definition is called pure virtual function.

---

# Syntax

```cpp
virtual void show()=0;
```

---

# Abstract Base Class

A class containing at least one pure virtual function becomes abstract class.

Objects of abstract class cannot be created.

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

class Shape
{
    public:

    virtual void area()=0;
};

class Circle : public Shape
{
    public:

    void area()
    {
        cout<<"Area of Circle";
    }
};

void main()
{
    Circle c;

    c.area();

    getch();
}
```

---

# Explanation

`Shape` is abstract class because it contains pure virtual function.

---

# Friend Function

A friend function is a function that is not a member of class but can access private and protected members.

Normally:
- Private data cannot be accessed outside class

But friend function gets special permission.

---

# Why Friend Function is Needed

Sometimes external functions need access to private data.

Example:
- Operator overloading
- Mathematical operations
- Comparing objects

---

# Syntax

```cpp
friend return_type function_name();
```

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

class Demo
{
    private:

    int x;

    public:

    Demo()
    {
        x=10;
    }

    friend void display(Demo);
};

void display(Demo d)
{
    cout<<"Value: "<<d.x;
}

void main()
{
    Demo d;

    display(d);

    getch();
}
```

---

# Explanation

- `display()` is not class member
- Still it accesses private variable `x`

---

# Characteristics of Friend Function

- Not member of class
- Declared using `friend`
- Can access private members
- Called like normal function

---

# Advantages of Friend Function

- Increases flexibility
- Useful in operator overloading
- Allows controlled access

---

# Disadvantages of Friend Function

- Reduces data security
- Breaks encapsulation

---

# Real Life Example

Suppose school principal gives special permission to auditor to access confidential records.

Similarly, friend function gets special permission.

---

# File Handling in C++

File handling means storing data permanently in files.

Without files:
- Data disappears after program ends

Files help:
- Save records
- Store information permanently
- Read and write data later

---

# Real Life Example

Suppose school stores student records in files.

Without files:
- Data lost after closing system

Similarly, programs use files for permanent storage.

---

# Types of Files

1. Text Files
2. Binary Files

---

# 1. Text Files

Store data in readable form.

Example:
```text
Rahul 101
```

---

# 2. Binary Files

Store data in machine-readable format.

Faster but not human readable.

---

# Streams in C++

A stream is a flow of data.

C++ uses streams for:
- Input
- Output
- File handling

---

# Types of Streams

| Stream | Purpose |
|---|---|
| cin | Input |
| cout | Output |
| ifstream | Input file stream |
| ofstream | Output file stream |
| fstream | Input and output file stream |

---

# Header File for File Handling

```cpp
#include<fstream.h>
```

---

# Writing Data to File

Uses:
- `ofstream`

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>
#include<fstream.h>

void main()
{
    ofstream fout;

    fout.open("student.txt");

    fout<<"Welcome to File Handling";

    fout.close();

    cout<<"Data Written";

    getch();
}
```

---

# Explanation

## `ofstream`

Used for writing file.

---

## `open()`

Opens file.

---

## `fout<<"text"`

Writes data into file.

---

## `close()`

Closes file.

---

# Reading Data from File

Uses:
- `ifstream`

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>
#include<fstream.h>

void main()
{
    ifstream fin;

    char ch;

    fin.open("student.txt");

    while(fin)
    {
        fin.get(ch);

        cout<<ch;
    }

    fin.close();

    getch();
}
```

---

# Explanation

Reads file character by character.

---

# File Operation Functions

---

# open()

Opens file.

---

# close()

Closes file.

---

# get()

Reads single character.

---

# put()

Writes single character.

---

# getline()

Reads entire line.

---

# read()

Reads binary data.

---

# write()

Writes binary data.

---

# seekg()

Moves input pointer.

---

# seekp()

Moves output pointer.

---

# tellg()

Returns current input position.

---

# tellp()

Returns current output position.

---

# File Opening Modes

| Mode | Meaning |
|---|---|
| ios::in | Input mode |
| ios::out | Output mode |
| ios::app | Append mode |
| ios::binary | Binary mode |

---

# Example with Append Mode

```cpp
#include<iostream.h>
#include<conio.h>
#include<fstream.h>

void main()
{
    ofstream fout;

    fout.open("data.txt",ios::app);

    fout<<"New Data\n";

    fout.close();

    getch();
}
```

---

# Templates in C++

Templates allow creation of generic functions and classes.

Templates work with multiple data types.

---

# Why Templates are Needed

Without templates:
- Separate functions needed for int, float, double etc.

Templates reduce duplicate code.

---

# Real Life Example

Suppose one water bottle can hold:
- Water
- Juice
- Milk

Similarly templates work with different data types.

---

# Function Template

---

# Syntax

```cpp
template <class T>
```

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

template <class T>

T add(T a,T b)
{
    return a+b;
}

void main()
{
    cout<<"Integer Sum: "<<add(10,20);

    cout<<"\nFloat Sum: "<<add(5.5,2.5);

    getch();
}
```

---

# Explanation

Same function works for:
- int
- float

---

# Class Template

Templates can also be used with classes.

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

template <class T>

class Demo
{
    T x;

    public:

    Demo(T a)
    {
        x=a;
    }

    void display()
    {
        cout<<"Value: "<<x;
    }
};

void main()
{
    Demo<int> d1(10);

    Demo<float> d2(5.5);

    d1.display();

    cout<<"\n";

    d2.display();

    getch();
}
```

---

# Advantages of Templates

- Code reuse
- Reduces duplication
- Improves flexibility
- Saves development time

---

# Exception Handling in C++

Exception handling is used to handle runtime errors.

Without exception handling:
- Program may crash

Exception handling makes programs safer.

---

# Real Life Example

Suppose car has airbags.

When accident happens:
- Airbags protect passengers

Similarly exception handling protects programs from crashing.

---

# Common Runtime Errors

- Divide by zero
- File not found
- Memory allocation failure
- Invalid input

---

# Keywords Used in Exception Handling

| Keyword | Purpose |
|---|---|
| try | Block containing risky code |
| throw | Throws exception |
| catch | Handles exception |

---

# Syntax

```cpp
try
{
}
catch(type variable)
{
}
```

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

void main()
{
    int a,b;

    cout<<"Enter Two Numbers: ";
    cin>>a>>b;

    try
    {
        if(b==0)
        {
            throw b;
        }

        cout<<"Result: "<<a/b;
    }

    catch(int x)
    {
        cout<<"Division by Zero Error";
    }

    getch();
}
```

---

# Explanation

- `try` contains risky code
- `throw` sends exception
- `catch` handles exception

---

# Advantages of Exception Handling

- Prevents program crash
- Improves reliability
- Easy error handling
- Better debugging

---

# Multiple Catch Blocks

Different errors can be handled separately.

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

void main()
{
    try
    {
        throw 10;
    }

    catch(int x)
    {
        cout<<"Integer Exception";
    }

    catch(...)
    {
        cout<<"Unknown Exception";
    }

    getch();
}
```

---

# Explanation

- First catch handles integer exception
- `catch(...)` handles unknown exceptions

---

# Important Points to Remember

- Virtual functions support runtime polymorphism.
- Friend functions access private members.
- File handling stores permanent data.
- Streams represent flow of data.
- Templates create generic code.
- Exception handling manages runtime errors.
- `try`, `throw`, and `catch` are used in exception handling.
- `ifstream` reads files.
- `ofstream` writes files.
- `fstream` performs both operations.

---

# Conclusion

Virtual functions make programs dynamic and support runtime polymorphism. Friend functions provide controlled access to private data. File handling allows permanent data storage and retrieval.

Templates improve code reusability by creating generic functions and classes. Exception handling makes programs reliable by handling runtime errors properly.

These concepts are extremely important in modern C++ programming and real-world software development because they improve flexibility, safety, efficiency, and maintainability of software systems.
