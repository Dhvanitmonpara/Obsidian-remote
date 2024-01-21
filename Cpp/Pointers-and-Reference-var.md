# Pointers 

Data type which holds the address of other data types.

```cpp
    int a=3;
    int* b;
    b = &a;

    cout<<"The value at address b is "<<*b<<endl;
    cout<<"The value at address b is "<<b<<endl;

```

In above code, when you use `b` it defines and prints address of `a` but when you use `*b` it points to `a` and prints value of `a`, so use `*b` instead of `b`.

xxxxxxxxxx #include<iostream>#include<iomanip>using namespace std;​int main(){ const char* a= "-";​    cout<<setw(9)<<a<<endl;    cout<<setw(8)<<a;    cout<<setw(2)<<a<<endl;    cout<<setw(7)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a<<endl;    cout<<setw(6)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a<<endl;    cout<<setw(5)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a<<endl;    cout<<setw(4)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a<<endl;    cout<<setw(3)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a<<endl;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a;    cout<<setw(2)<<a<<endl;    ​return 0;}​​cpp

# Pointer to pointer

```cpp
    int** c = &b;
    cout<<"The address of b is "<<&b<<endl;
    cout<<"The address of b is "<<c<<endl; 
    cout<<"The value at address c is "<<*c<<endl; 
    cout<<"The value at address value_at(value_at(c)) is "<<**c<<endl; 
```
