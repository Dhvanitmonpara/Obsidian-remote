# Classes and objects

C++ --> initially called --> C with classes by stroustroup
class --> extension of structures (in C)
structures had limitations

members are public

No methods

- classes --> structures + more
- classes --> can have methods and properties
- classes --> can make few members as private & few as public
- structures in C++ are typedefed

<br>

# Class declaration

```cpp

    class student {

        // declaration and logic
        int roll_no;

    }

    int main() {

        student Aman;  // object declaration

        // value inserting and function calling
        Aman.roll_no = 20;

    }


```

Example:

```cpp
    class student {

        private:    // private
        int roll;
        bool fees;
        
        public:     // public
        string name;
        string city;

        // function prototype to insert data
        void setData(int num, bool paidfees);

        void getData() {
            cout<<endl<<roll;
            cout<<endl<<fees;
            cout<<endl<<name;
            cout<<endl<<city;
        }
    }

    // function to insert data (watch video number 21 of C++ playlist by codewithharry for better understanding)

    void student :: setData(int num, bool paidfees) {
        roll = num;
        fees = paidfees;
    }

    // main function
    int main() {

        student Aman;   // object declaration

        // values insertion
        Aman.name = "Aman";
        Aman.city = "Ahmedabad";

        // functions
        setData(1, true);
        getData()
    }

```

Or pogrammer can directly declare object within classes like this:

```cpp

class Employee{
            // Class definition
} harry, rohan, lovish;

```

<br>

# Nested functions

Programmer can use functions inside other functions.
For this example `chk_bin()` is nested function under `ones_compliment()`

```cpp
#include <iostream>
#include <string>
using namespace std;

class binary
{
private:
    string s;
    void chk_bin(void);

public:
    void read(void);
    void ones_compliment(void);
    void display(void);
};

void binary::read(void)
{
    cout << endl << "Enter a binary number => ";
    cin >> s;
}

void binary::chk_bin(void)
{
    for (int i = 0; i < s.length(); i++)
    {
        if (s.at(i) != '0' && s.at(i) != '1')
        {
            cout << "Incorrect binary format" << endl;
            exit(0);
        }
    }
}

void binary::ones_compliment(void)
{
    chk_bin();
    for (int i = 0; i < s.length(); i++)
    {
        if (s.at(i) == '0')
        {
            s.at(i) = '1';
        }
       else
        {
            s.at(i) = '0';
        }
    }
}

void binary::display(void)
{
    cout<<"Displaying your binary number : ";
    for (int i = 0; i < s.length(); i++)
    {
        cout << s.at(i);
    }
    cout<<endl;
}

int main()
{
    binary b;
    b.read();
    // b.chk_bin();
    b.display();
    b.ones_compliment();
    b.display();

    return 0;
}

```