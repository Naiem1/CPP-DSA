# Pointer
## **Pointer**
**`Pointer is a variable which is use for storing address of data`**

types of variable
1. data Variable - store data
2. Address variable - storing memory address

if i declare a variable like below: - 
```cpp
// This is integer type variable x have value 10
  int x = 10; // storing value 10, this is data variable


// I declare a variable it occupy some memory depending on the size of integer

// how to declare a pointer variable
int *p; //this is address variable. it can not store data. it only store address of the data and it own address is 3001


// Now if I say p Assign `&x` so what is the address of x let's assume 2001 that 2001 is store in p; so there is 2001 pointing x;
p = &x;
// it not having data but having the data address of X and it pointing on X, showing location of X, so that's we call it pointer
```

### Syntax of pointer
- if I write `int *P;` this is the declaration of address variable ***thats pointer***.
- And `p = &x;` this is initialization of a pointer variable.

```cpp
// let's assume memory address of x = 2001, and 
// p = 3001 :- p is also variable so it is also having it own memory address
int x = 10;
int *p; // Declaration of address variable
p = &x; // Initialization of a pointer variable

// Printing
cout << x; // 10;
cout << &x; // 2001
cout << p; // 2001 - [pointing the address of x;]
cout << &p; // 3001, [Print p variable address, p is also variable so it is also having it own memory address]
cout << *p; // 10, [p is pointing 2001 and the value of this address 10; this called dereferencing or accessing the data where p is pointing]
```

**For pointer there are 3 statement is most important**
  1. **Declaration**
      - *Declaration of a pointer is little deferent from normal variables that we write **`*P`** in front of it.*

      ```cpp
      int *p; // Declaration of pointer

      ```
 2. **Initialization**
    ```cpp
      p = &x; // if we already have existing variable we can use this one
    ```
 3. **Dereferencing**
    - *Dereferencing means `wherever pointer is pointing` you are `going that location and accessing the data.`* pointer is referring there.
    - *`Dereferencing means going the that location and taking the data. `*if we doing that we must we `*P`
    ```cpp
      cout << *p; // this *P called as dereferencing
    ```
***`Note:`*** &a == p; ***pointing the same address***
## What is the Purpose of pointer or user case of pointer

- Pointer is address variable
- It can store the address of data•Pointer are used for accessing heap memory
- 5 Arithmetic operations are allowed pointer
- p++ - move pointer to next element
- p-- move pointer to previous element
- p+k  gives address of kth element form pointer location to right
- p-k  gives address of kth element from pointer location to left
- q-p  gives number of elements between 2 pointers p and q
- Pointers can be of many levels
- Double pointer is used for accessing 2D arrays

### Program to Demonstrate Pointer Syntax

```cpp
#include <iostream>
using namespace std;
int main() {

  int a=10;
  int *p=&a;

  cout<<a<<endl;
  cout<<&a<<endl;
  cout<<p<<endl;
  cout<<*p<<endl;

  return0;
}
```

## Why Pointer

## Array of Pointer
```C++
  #include <bits/stdc++.h>
  using namespace std;

  int main() {
    // Write C++ code here
   int marks[5] = {10, 20, 30, 40, 50};
   
   cout << marks << "\n"; // 0x7ffc049eddc0 - 1st address
   cout << marks + 1 << "\n"; // 0x7ffc049eddc4 - 2nd address
   cout << *marks << endl; // 10
   cout << *marks + 1 << endl; // 11
   cout << *(marks + 1) << endl; // 20
   
   for (int i = 0; i < 5; i++) {
       cout << *marks + i << " "; // 10 20 30 40 50
   }
   
   cout << endl;
   
   int *p = marks; 
   cout << *p << endl; // 10
   
   for (int i = 0; i < 5; i++) {
       cout << *( p + i) << " "; // 10 20 30 40 50
   }
   
    cout << endl;
  
   cout << sizeof(marks) / sizeof(marks[0]) << endl; // 5
   cout << sizeof(p) / sizeof(marks[0]) << endl; // 2
   
   cout << &marks << endl; // 0x7ffc049eddc0 - 1st address of an array
   cout << &marks[0] << endl; // 0x7ffc049eddc0 - 2nd address of an array
   cout << &p  << endl; // 0x7ffc049eddb8 - pointer address
   
   cout << "==================" << endl;
   cout << marks++ << endl; // error
   marks = marks + 1; // error
   cout << *p++ << endl; // 10
    for (int i = 0; i < 5; i++) {
         cout << *p++ << " "; // 10 20 30 40 50
     }



      return 0;
  }
```
