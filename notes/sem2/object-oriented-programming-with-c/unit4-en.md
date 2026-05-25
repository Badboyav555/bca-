# UNIT 4 – Inheritance, Derived Classes, Pointers and Dynamic Memory Management in C++



# Introduction to Inheritance

Inheritance is one of the most important features of Object Oriented Programming (OOP). Inheritance allows one class to acquire properties and functions of another class.

The main purpose of inheritance is:
- Code reusability
- Faster development
- Better organization
- Reduced redundancy

Using inheritance, programmers can reuse already existing code instead of writing same code again and again.

---

# Real Life Example of Inheritance

Suppose there is a class called `Animal`.

Animal has common properties:
- eat()
- sleep()
- breathe()

Now different animals like:
- Dog
- Cat
- Cow

can inherit these properties.

Dog can also have its own function:
- bark()

Cat can have:
- meow()

Thus:
- Common features are inherited
- Special features remain unique

---

# Base Class and Derived Class

## Base Class

The class whose properties are inherited is called:
- Base Class
- Parent Class
- Super Class

---

## Derived Class

The class that inherits properties is called:
- Derived Class
- Child Class
- Sub Class

---

# Syntax of Inheritance

```cpp
class DerivedClass : access_specifier BaseClass
{
};
```

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

class Animal
{
    public:

    void eat()
    {
        cout<<"Animal can eat\n";
    }
};

class Dog : public Animal
{
    public:

    void bark()
    {
        cout<<"Dog can bark";
    }
};

void main()
{
    Dog d;

    d.eat();
    d.bark();

    getch();
}
```

---

# Explanation

## `class Animal`

Base class.

---

## `class Dog : public Animal`

Dog inherits Animal publicly.

---

## `d.eat()`

Dog object can access inherited function.

---

## `d.bark()`

Dog has its own function also.

---

# Advantages of Inheritance

- Code reuse
- Reduces duplicate code
- Easy maintenance
- Better software organization
- Faster development

---

# Types of Inheritance

1. Single Inheritance
2. Multiple Inheritance
3. Multilevel Inheritance
4. Hierarchical Inheritance
5. Hybrid Inheritance

---

# 1. Single Inheritance

One derived class inherits one base class.

---

# Example

```cpp
class A
{
};

class B : public A
{
};
```

---

# Real Life Example

Father → Son

Only one child inherits one parent.

---

# 2. Multiple Inheritance

One derived class inherits multiple base classes.

---

# Example

```cpp
class A
{
};

class B
{
};

class C : public A, public B
{
};
```

---

# Real Life Example

A student learns:
- Mathematics from one teacher
- Science from another teacher

Knowledge comes from multiple sources.

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

class Father
{
    public:

    void house()
    {
        cout<<"Father's House\n";
    }
};

class Mother
{
    public:

    void jewelry()
    {
        cout<<"Mother's Jewelry\n";
    }
};

class Child : public Father, public Mother
{
};

void main()
{
    Child c;

    c.house();
    c.jewelry();

    getch();
}
```

---

# 3. Multilevel Inheritance

Inheritance chain is formed.

---

# Example

```cpp
class A
{
};

class B : public A
{
};

class C : public B
{
};
```

---

# Real Life Example

Grandfather → Father → Son

Properties transfer generation to generation.

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

class Grandfather
{
    public:

    void land()
    {
        cout<<"Land Property\n";
    }
};

class Father : public Grandfather
{
};

class Son : public Father
{
};

void main()
{
    Son s;

    s.land();

    getch();
}
```

---

# 4. Hierarchical Inheritance

Multiple classes inherit one base class.

---

# Example

```cpp
class A
{
};

class B : public A
{
};

class C : public A
{
};
```

---

# Real Life Example

One parent with multiple children.

---

# 5. Hybrid Inheritance

Combination of different inheritances.

---

# Access Specifiers in Inheritance

Access specifiers control accessibility of inherited members.

Three types:
1. Public
2. Private
3. Protected

---

# 1. Public Access Specifier

Public members can be accessed from outside class.

---

# Example

```cpp
class Demo
{
    public:

    int x;
};
```

---

# 2. Private Access Specifier

Private members cannot be accessed directly outside class.

---

# Example

```cpp
class Demo
{
    private:

    int x;
};
```

---

# 3. Protected Access Specifier

Protected members can be accessed inside derived classes.

---

# Example

```cpp
class Demo
{
    protected:

    int x;
};
```

---

# Public Inheritance

When inheritance is public:
- Public members remain public
- Protected members remain protected

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

class A
{
    public:

    int x;
};

class B : public A
{
};

void main()
{
    B obj;

    obj.x=10;

    cout<<obj.x;

    getch();
}
```

---

# Private Inheritance

When inheritance is private:
- Public members become private
- Protected members become private

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

class A
{
    public:

    int x;
};

class B : private A
{
    public:

    void setData()
    {
        x=10;

        cout<<x;
    }
};

void main()
{
    B obj;

    obj.setData();

    getch();
}
```

---

# Derived Class Constructors

Constructors are not inherited automatically.

But derived class constructor can call base class constructor.

---

# Why Needed?

Base class data should initialize before derived class data.

---

# Syntax

```cpp
Derived(parameters) : Base(parameters)
{
}
```

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

class Base
{
    int x;

    public:

    Base(int a)
    {
        x=a;

        cout<<"Base Constructor\n";
    }
};

class Derived : public Base
{
    int y;

    public:

    Derived(int a,int b) : Base(a)
    {
        y=b;

        cout<<"Derived Constructor";
    }
};

void main()
{
    Derived d(10,20);

    getch();
}
```

---

# Output

```text
Base Constructor
Derived Constructor
```

---

# Explanation

Base constructor executes first.

Then derived constructor executes.

---

# Abstract Base Class

An abstract base class is a class that contains at least one pure virtual function.

Objects of abstract class cannot be created.

It is used only for inheritance.

---

# Pure Virtual Function

Syntax:

```cpp
virtual void show() = 0;
```

---

# Real Life Example

Suppose class `Shape`.

Different shapes:
- Circle
- Rectangle
- Triangle

All have different area calculations.

So base class only defines structure.

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

# Ambiguity in Inheritance

Ambiguity occurs when compiler gets confused about which member to use.

Usually happens in multiple inheritance.

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

class A
{
    public:

    void show()
    {
        cout<<"Class A\n";
    }
};

class B
{
    public:

    void show()
    {
        cout<<"Class B";
    }
};

class C : public A, public B
{
};

void main()
{
    C obj;

    obj.A::show();

    obj.B::show();

    getch();
}
```

---

# Explanation

Both classes contain `show()`.

Compiler becomes confused.

Scope resolution operator solves ambiguity.

---

# Member Functions in Inheritance

Derived classes can:
- Use inherited functions
- Override functions
- Create new functions

---

# Function Overriding Example

```cpp
#include<iostream.h>
#include<conio.h>

class Animal
{
    public:

    void sound()
    {
        cout<<"Animal Sound\n";
    }
};

class Dog : public Animal
{
    public:

    void sound()
    {
        cout<<"Dog Bark";
    }
};

void main()
{
    Dog d;

    d.sound();

    getch();
}
```

---

# Pointers in C++

A pointer is a variable that stores address of another variable.

---

# Why Pointers are Important

Pointers help in:
- Dynamic memory allocation
- Fast data access
- Arrays and strings
- Functions
- Object handling

---

# Real Life Example

Suppose house address:
- House = Variable
- Address = Pointer

Pointer stores location, not actual value.

---

# Syntax of Pointer

```cpp
data_type *pointer_name;
```

---

# Example

```cpp
int *p;
```

---

# Address Operator (&)

Used to get address of variable.

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

void main()
{
    int x=10;

    cout<<"Value: "<<x;

    cout<<"\nAddress: "<<&x;

    getch();
}
```

---

# Pointer Initialization

```cpp
int x=10;

int *p=&x;
```

Here:
- `p` stores address of `x`

---

# Dereference Operator (*)

Used to access value stored at address.

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

void main()
{
    int x=10;

    int *p=&x;

    cout<<"Value of x: "<<*p;

    getch();
}
```

---

# Explanation

`*p` accesses value stored at address.

---

# Pointers and Strings

Pointers can work with strings.

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

void main()
{
    char name[]="Rahul";

    char *p=name;

    cout<<p;

    getch();
}
```

---

# Explanation

Pointer stores address of first character.

---

# Pointer Arithmetic

Pointers can move through memory.

Operations:
- Increment
- Decrement
- Addition
- Subtraction

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

void main()
{
    int arr[]={10,20,30};

    int *p=arr;

    cout<<*p;

    p++;

    cout<<"\n"<<*p;

    getch();
}
```

---

# Dynamic Memory Management

Dynamic memory allocation means allocating memory during runtime.

C++ uses:
- `new`
- `delete`

operators.

---

# Why Dynamic Memory Allocation is Needed

Sometimes memory requirement is unknown during compilation.

Example:
- User-defined array size
- Dynamic objects
- Games
- Databases

---

# new Operator

Allocates memory dynamically.

---

# Syntax

```cpp
pointer = new data_type;
```

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

void main()
{
    int *p;

    p=new int;

    *p=100;

    cout<<"Value: "<<*p;

    getch();
}
```

---

# Explanation

- Memory allocated dynamically
- Pointer stores memory address

---

# delete Operator

Used to free dynamically allocated memory.

---

# Syntax

```cpp
delete pointer;
```

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

void main()
{
    int *p;

    p=new int;

    *p=50;

    cout<<"Value: "<<*p;

    delete p;

    getch();
}
```

---

# Why delete is Important

Without delete:
- Memory waste occurs
- Memory leak happens

---

# Real Life Example of new and delete

Suppose hotel room booking:
- `new` = booking room
- `delete` = vacating room

If room never vacated:
- Resources wasted

---

# Dynamic Array Allocation

```cpp
int *arr;

arr=new int[5];
```

---

# Freeing Array Memory

```cpp
delete[] arr;
```

---

# Example Program

```cpp
#include<iostream.h>
#include<conio.h>

void main()
{
    int *arr;

    arr=new int[3];

    arr[0]=10;
    arr[1]=20;
    arr[2]=30;

    cout<<arr[0];
    cout<<"\n"<<arr[1];
    cout<<"\n"<<arr[2];

    delete[] arr;

    getch();
}
```

---

# Important Points to Remember

- Inheritance improves code reuse.
- Base class provides common features.
- Derived class acquires properties.
- Public inheritance keeps accessibility same.
- Private inheritance changes accessibility.
- Constructors initialize objects.
- Abstract class contains pure virtual function.
- Ambiguity occurs in multiple inheritance.
- Pointer stores address.
- `&` gives address.
- `*` accesses value.
- `new` allocates memory.
- `delete` frees memory.

---

# Conclusion

Inheritance is one of the most powerful features of Object Oriented Programming because it allows code reuse and better organization. Derived classes can inherit features from base classes and extend functionality.

Pointers are extremely important in C++ because they provide direct memory access and support dynamic memory management. Operators like `new` and `delete` allow programs to allocate and free memory during runtime, making software more flexible and efficient.

These concepts form the core of advanced C++ programming and are heavily used in real-world software development.
