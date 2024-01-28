# Types of Inheritance in OOP

## Single Inheritance

- A class inherits from only one base class.
- Parent-child relationship is one-to-one.
- [Click here for Single Inheritance diagram](https://www.trytoprogram.com/images/single-inheritance.jpg)

## Multiple Inheritance

- A class inherits from more than one base class.
- Allows a derived class to inherit attributes and methods from multiple parent classes.
- [Click here for Multiple Inheritance diagram](https://www.trytoprogram.com/images/multiple-inheritance.jpg)

## Hierarchical Inheritance

- Multiple classes inherit from a single base class.
- Forms a hierarchy where a base class is inherited by several derived classes.
- [Click here for Hierarchical Inheritance diagram](https://www.trytoprogram.com/images/heirarchical-inheritance.jpg)

## Multilevel Inheritance

- A class inherits from another class, and then a new class inherits from that derived class.
- Forms a chain of inheritance.
- [Click here for Multilevel Click here for diagram diagram](https://www.trytoprogram.com/images/multi-level-inheritance.jpg)

## Hybrid Inheritance

- Combination of multiple types of inheritance, such as single, multiple, hierarchical, or multilevel.
- Used to model complex relationships in certain scenarios.
- [Click here for Hybrid Inheritance diagram](https://www.trytoprogram.com/images/hybrid-inheritance.jpg)

<br>

# Syntax

```
class {{Dervied-class-name}} : {{access-modifier}} {{Base-class-name}} {

}
```

**Private class:** All the members will be private.

**Public class:** All the members will be public.

**Protected class:** All the member are private but inheritable.

In summary derived class can't access private members of base class even it defined as private. Private is default class-access.

```
// For Multiple Inheritance

class {{Dervied-class-name}} : {{access-modifier}} {{Base-class-1}}, {{access-modifier}} {{Base-class-2}} {

}
```

## Derivation table

| Derivation        | Public Derivation | Private Derivation | Protected     |
| ----------------- | ----------------- | ------------------ | ------------- |
| Private members   | Not Inherited     | Not Inherited      | Not Inherited |
| Protected members | Protected         | Private            | Protected     |
| Public members    | Public            | Private            | Protected     |

<br>

```cpp
#include <iostream>
using namespace std;

// Base Class
class Employee
{
public:
    int id;
    float salary;
    Employee(int inpId)
    {
        id = inpId;
        salary = 34.0;
    }
    Employee() {}
};

// Creating a Programmer class derived from Employee Base class
class Programmer : public Employee
{
public:
    int languageCode;
    Programmer(int inpId)
    {
        id = inpId;
        languageCode = 9;
    }
    void getData(){
        cout<<id<<endl;
    }
};

int main()
{
    Employee harry(1), rohan(2);
    cout << harry.salary << endl;
    cout << rohan.salary << endl;
    Programmer skillF(10);
    cout << skillF.languageCode<<endl;
    cout << skillF.id<<endl;
    skillF.getData();
    return 0;
}

```

Classes example

```cpp
#include <iostream>
using namespace std;

class Base
{
    int data1; // private by default and is not inheritable
public:
    int data2;
    void setData();
    int getData1();
    int getData2();
};

void Base ::setData(void)
{
    data1 = 10;
    data2 = 20;
}

int Base::getData1()
{
    return data1;
}

int Base::getData2()
{
    return data2;
}

class Derived : public Base
{ // Class is being derived publically
    int data3;

public:
    void process();
    void display();
};

void Derived ::process()
{
    data3 = data2 * getData1();
}

void Derived ::display()
{
    cout << "Value of data 1 is " << getData1() << endl;
    cout << "Value of data 2 is " << data2 << endl;
    cout << "Value of data 3 is " << data3 << endl;
}

int main()
{
    Derived der;
    der.setData();
    der.process();
    der.display();

    return 0;
}

```
# Ambiguity reslution

Ambiguity in inheritance can be defined when one class derived for two or more base classes then there are chances that the base classes have functions with the same name. so it will confuse derived class to choose from similar name functions. To solve this ambiguity scope resolution operator is used `::`.

```cpp
#include <iostream>
using namespace std;

class Base1{
    public:
        void greet(){
            cout<<"How are you?"<<endl;
        }
};

class Base2{
    public:
        void greet()
        {
            cout << "Kaise ho?" << endl;
        }
};


class Derived : public Base1, public Base2{
   int a;
   public:
    void greet(){
        Base2 :: greet();
    }
};

int main(){
  // Ambibuity 1
     Base1 base1obj;
     Base2 base2obj;
     base1obj.greet();
     base2obj.greet();
     Derived d;
     d.greet();

    return 0;
}

class B{
    public:
        void say(){
            cout<<"Hello world"<<endl;
        }
};

class D: public B{
    int a;
    // D's new say() method will override base class's say() method
    public:
        void say()
        {
            cout << "Hello my beautiful people" << endl;
        }
};

int main(){
    // Ambibuity 2
    B b;
    b.say();

    D d;
    d.say();

    return 0;
}

```