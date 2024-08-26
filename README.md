# Experiment-10

**Aim:** <br>
To study and implement Pointer Operations (call by value and call by reference) <br>
<br>
**Theory:** <br>
There are two ways to call a variable to a function for various operations. <br>
| Call by Value  | Call by Reference |
| ------------- | ------------- |
| A method of passing arguments to a function where the actual value is passed.  | A method of passing arguments where the address of the variable is passed.  |
| Does not affect the original variable.  | Does affect the original variable.  |
| More memory is used because a copy of the actual value is made.  | Less memory is used because only the address is passed.  |
| Used when the function does not need to modify the original data.  | Used when the function needs to modify the original data or when passing large objects.  |
<br>

**Code:** <br>
<br>
a.<br>

```
#include <iostream>
using namespace std;

//call by value
int a,b;
void swap (int a, int b)
{
    int sw;
    sw = a;
    a = b;
    b = sw;
    cout<<"Swapped Values: "<<endl;
    cout<<"a: "<<a<<endl;
    cout<<"b: "<<b<<endl;
}

int main()
{
    int a,b;
    cout<<"Using call by value: "<<endl;
    cout<<"Enter a number: ";
    cin>>a;
    cout<<"Enter another number: ";
    cin>>b;
    cout<<"User Values: "<<endl;
    cout<<"a: "<<a<<endl;
    cout<<"b: "<<b<<endl;
    swap(a,b);
    
}
    
```
<br>

b.<br>

```
#include <iostream>
using namespace std;

//call by value
int a,b;
int *pa, *pb;
void swapr (int *pa, int *pb)
{
    int *psw;
    int sw;
    psw = &sw;
    *psw = *pa;
    *pa = *pb;
    *pb = *psw;
    cout<<"Swapped Values: "<<endl;
    cout<<"a: "<<*pa<<endl;
    cout<<"b: "<<*pb<<endl;
}

int main()
{
    int a,b;
    int *pa, *pb;
    cout<<"Using call by value: "<<endl;
    cout<<"Enter a number: ";
    cin>>a;
    pa = &a;
    cout<<"Enter another number: ";
    cin>>b;
    pb = &b;
    cout<<"User Values: "<<endl;
    cout<<"a: "<<a<<endl;
    cout<<"b: "<<b<<endl;
    swapr(pa,pb);
    
}

```
<br>

**Conclusion:** <br>
&#8594; We learnt about call by value and call by reference in C++. <br>
&#8594; We learnt the use case of each in C++. <br>
*******
