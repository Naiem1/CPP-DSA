# CPP Arrays
**Declaring Array**
```C++
  #include <iostream>
  using namespace std;
  
  int main() {
    int A[5]; // Array Declaring
    
    for (int i = 0; i < 5; i++)
      cout << A[i]; // Print random Garbage Value
    

    // Array Initialization
    int A[5] = { 1, 3, 3, 4, 5}; 

  }
```

**Array Declaring and Initialization**
```C++
  #include <iostream>
  using namespace std;
  
  int main() {
    // Array Declaring and Initialization
    int A[5] = {1, 2, 3, 4, 5};
    
    for (int i = 0; i < 5; i++)
      cout << A[i]; // Print initialized Value
  }
```

```C++
#include <iostream>
using namespace std;

int main() {
  int A[5];
  for (int = 0; i < 5; i++) 
    cout << A[i]; // print garbage value

}
```

```C++
#include <iostream>
using namespace std;

int main() {
  int A[5] = {3, 4, 10, 12, 5};
  for (int = 0; i < 5; i++) 
    cout << A[i]; // print 3 4 10 12 5

}
```

```C++
#include <iostream>
using namespace std;

int main() {
  int A[5] = {};
  for (int = 0; i < 5; i++) 
    cout << A[i]; // print 0 0 0 0 0

}
```

```C++
#include <iostream>
using namespace std;

int main() {
  int A[5] = {0};
  for (int = 0; i < 5; i++) 
    cout << A[i]; // print 0 0 0 0 0

}
```

```C++
#include <iostream>
using namespace std;

int main() {
  int A[5] = {3, 4, 10,};
  for (int = 0; i < 5; i++) 
    cout << A[i]; // print 3 4 10 0 0

}
```

```C++
#include <iostream>
using namespace std;

int main() {
  int A[5] = {3, 4, 10, 12, 15};
  for (int = 0; i < 5; i++) 
    cout << A[i]; // print 3 4 10 0 0

}
```
### If we give element more than of an array size
- I have 5 value here if I give extra more value that mean exact of array element. compiler give error (compiler error)
- We can not have array element more than of an array size.

```C++
#include <iostream>
using namespace std;

int main() {
  int A[5] = {3, 4, 10, 12, 15, 20};
  for (int = 0; i < 5; i++) 
    cout << A[i]; // compiler time error
}
```

### **Dynamic Array size**
- If we do not give array size. It also allow us to create array.

```C++
#include <iostream>
using namespace std;

int main() {
  int A[] = {3, 4, 10, 13, 15};
  for (int = 0; i < 5; i++) 
    cout << A[i]; // print 3 4 10 13 15

}
```


## ForEach Loop
```C++
#include <iostream>
using namespace std;

int main() {
  int A[] = {3, 4, 10, 13, 15};
  for (int X:A) ;
    cout << X << endl; // print 3 4 10 13 15

}
```

- It will Iterating all the element one by one. each an element taken x.
- ***No need to array size***


### Array float
```C++
#include <iostream>
using namespace std;

int main() {
  float A[] = {3.5f, 4.6f, 10, 13, 15};
  for (int X:A) 
    cout << X; // print 3 4 10 13 15, because x is int data type

}
```

- if we want to print float value
  

```C++
#include <iostream>
using namespace std;

int main() {
  float A[] = {3.5f, 4.6f, 10, 13, 15};
  for (float X:A) 
    cout << X; // print 3.5 4.6 10 13 15

}
```

- We use `auto` keyword instead of data type
  
```C++
#include <iostream>
using namespace std;

int main() {
  int A[] = {3, 4, 10, 13, 15};
  for (auto X:A) // here dynamically find data type
    cout << X; // print 3 4 10 13 15

}
```

## character data

```C++
#include <iostream>
using namespace std;

int main() {
  char A[] = {'A', 66, 'C', 68};
  for (auto X:A) // here dynamically find data type
    cout << X; // print A B C D

}
```

- without `auto`
  
```C++
#include <iostream>
using namespace std;

int main() {
  char A[] = {'A', 66, 'C', 68};
  for (int X:A) // type casting using int
    cout << X; // print 65, 66, 77, 68

}
```


---

`A[] = {4, 7, 6, 9, 5, 2, 7}`
`max = 4; n = 7`

|i|A[i]|`if(A[i]>max); max = A[i]`|
|---|---|---|
| 0 | 4 | 4 |
| 1 | 8 | 8 |
| 2 | 6 | 8 |
| 3 | 9 | 9 |
| 4 | 5 | 9 |
| 5 | 2 | 9 |
| 6 | 7 | 9 |


### Maximum Number of an Array
```cpp
#include <iostream>
using namespace std;

int main() {
  int A[5] = {2, 4, 10, 50, 100};

  int max = INT_MIN; // Minimum Number
  for (auto x:A) 
      if (x > min)
        max = x;
        cout << "Maximum Number is: " << max << endl;

  return 0;
}

```

### Minimum Number of an Array
```cpp
#include <iostream>
using namespace std;

int main() {
  int A[5] = {2, 4, 10, 50, 100};

  int min = INT_MAX; // Maximum Number
  for (auto x:A) 
      if (x < min)
        min = x;
        cout << "Minimum Number is: " << min << endl;

  return 0;
}

```

---

## Searching
*`Searching` is a process of a finding location of an element*
  
**There are two search method**
  1. **Linear Search Method**
  2. **Binary Search Method**

### **Linear Search**

- List of elements
- List of elements store in array
- Array of size 10 
- I want to search of an element
- searching element usually called `key`
- Find the `location` of key that mean `index`
- what is the index of key / where it is i want to find out
- I want to find out index of the element

`int A[10]] = {6, 11, 25, 7, 15, 6, 12, 20, 9, 14};`

```cpp
int A[10]; n = 10, key; 
cout << "Enter Numbers: ";
for (int i = 0; i < n; i++) {
  cout >> A[i];
}

cout << "Enter Key: ";
cin >> key;
for (int i = 0; i < n; i++) {
  if (A[i] == key) {
    cout << "Found at" << i;
    return 0;
  }
}
cout << "Not Found!";

```

### Program for Linear Search#include
```CPP
<iostream>
using namespace std;
int main(){
  int A[10]={2, 4, 6, 8, 12, 3, 5, 7, 9};
  int key; 
  cout << "Enter a Key element "; 
  cin >> key;
  for(int i=0;i<10;i++) {
    if(key == A[i])  {   
       cout<<"The Key element is found at "<<i<<endl;   
       exit(0);  
      } 
    } 
    cout<<"Key element not found" << endl;
    return 0;
}
```
**Linear Search - Search every element one by one until reach the element**

### **Binary Search**
- In Binary search method one compulsory condition that is one thing is mandatory ***`Element must be sorted order`*** then we can perform binary search.
- Requirement of binary search algorithms -> Array should be shorted

**producer**
```cpp
int n = 5, l, r, mid;
int A[5] = {1, 2, 3, 4, 5};

```
1. At first we are going to take two variable `l` and `r`
   - Here `l` ➜ is left and value is `0`
   - `r` ➜ is right and value is `n - 1`
  
2. Now we are going to find **mid position** of an array
   
   ```cpp
   int mid = l - 4 / 2 // give floor value 
   ```

|    l   |   r   |   mid = [l + r / 2]   |
|--------|-------| ------- | 
|   0    |   9   |    4    |


- Here 3 cases can be there
  - case i :  data == mid
  - case ii : data < mid
  - case iii: data > mid
  ### if,  data > mid 
   -  data present **`mid to right`**
   -  so, now new value of `l` is `mid + 1` so, `l = mid + 1 `

  ### if, data < mid
  - data present **`mid to left`**
  - so, now new value of `l` is remain as it is and `r` is `mid - 1` so, `r = mid - 1`

- when `l`, `r` and `mid` become same we get the result


### if `l` value becomes grater then `r` value `if(l > r)` it's means data is not present 

### Binary Search Code


```JavaScript
  const arr = [10, 20, 30, 40, 50, 60, 70, 80, 90, 100];

let l = 0; 
let r = arr.length - 1;
let key = 80;
let isFound = false;

while (l <= r) {
  let mid = (l + r) / 2 | 0;
  console.log(mid);

  console.log(l, r)
  
  if (key === arr[mid]) {
    console.log('Data Found at:', mid);
    isFound = true;
    break;
  } else if (key > arr[mid]) {
    l = mid + 1;
  } else {
    r = mid - r;
  }
}

if (!isFound) {
  console.log('Not Found!');
}
``` 

## Questions
1. Binary Search
2. Order Agonistic Binary Search
3. 1'st and last occurrence of and Elements in sorted array
4. count of element in a sorted array
5. #Number of tries - array is rotated
6. Find and Element in sorted array
7. Searching in needly sorted array


## Nested For Loop
```cpp
for (int i = 0; i < 3; i++) {
  for (int j = 0; j < 3; j++)
    cout << j;
}
```
|  i   |   j   |
|------|-------|
|**0** |   0   |
|      |   1   |
|      |   2   |
|      |   3   |
|**1** |   0   |
|      |   1   |
|      |   2   |
|      |   3   |
|**2** |   0   |
|      |   1   |
|      |   2   |
|      |   3   |

```cpp
#include <iostream>
using namespace std;

int main() {
  for (int i = 0; i < 3; i++) {
    for (int j = 0; i <= 5; j++) {
      cout << "(" << "," << j << ") ";
    }
    cout < endl;
  }
  
  return 0;
}

// Printing
(1,1) (1,2) (1,3) (1,4) (1,5)
(2,1) (2,2) (2,3) (2,4) (2,5)
(3,1) (3,2) (3,3) (3,4) (3,5)
```

|  0   |   1   |   2   |    3  |
|------|-------|-------|-------|
|   1  |   2   |  3    |   4   |
|      |   1   |       |       |
|      |   2   |       |       |


---

## Multidimensional Array

### **2D Array**
```cpp
  int A[2][3] = {{2, 5, 9}, {6, 9, 15}};

  for (int i = 0; i < 0; i ++) {
    for (int j = 0; j < 0; j++) {
      cout << j;
    }
  }
```

```cpp
#include <iostream>
using namespace std;

int main()
{

  int A[2][3] = {{2, 4, 6}, {3, 5, 7}};

  for (int i = 0; i < 2; i++)
  {
    for (int j = 0; j < 3; j++)
    {
      cout << A[i][j] << " ";
    }
    cout << endl;
  }
  return 0;
}

// printing 
  2 4 6 
  3 5 7
```

```cpp
#include <iostream>
using namespace std;

int main()
{

  int A[2][3] = {2, 4, 6, 3, 5, 7}; // same it automatically detect row and column

  for (int i = 0; i < 2; i++)
  {
    for (int j = 0; j < 3; j++)
    {
      cout << A[i][j] << " ";
    }
    cout << endl;
  }
  return 0;
}

// printing 
  2 4 6 
  3 5 7
```

```cpp
#include <iostream>
using namespace std;

int main()
{
  // same it automatically detect row and column
  // but last 2 digit print 0
  int A[2][3] = {2, 4, 6, 3}; 

  for (int i = 0; i < 2; i++)
  {
    for (int j = 0; j < 3; j++)
    {
      cout << A[i][j] << " ";
    }
    cout << endl;
  }
  return 0;
}

// printing 
  2 4 6 
  3 0 0
  
```

## 2D Array Accessing using ForEach loop

```cpp
#include <iostream>
using namespace std;

int main()
{
  // same it automatically detect row and column
  int A[2][3] = {2, 4, 6, 3, 5, 7}; 

  // using forEach loop for 2d Array must using reference
  for(auto& x:A) {
    for(auto& y:x) {
      cout << y << " ";
    }
    cout << endl;
  }

  
  return 0;
}

// printing 
  2 4 6 
  3 5 7
  
```

### Input an Array
```cpp
#include <iostream>
using namespace std;

int main()
{
  // same it automatically detect row and column
  int A[2][3]; 

  // using forEach loop for 2d Array must using reference
  for(auto& x:A) {
    for(auto& y:x) {
      cin << y;
    }
  }
  for(auto& x:A) {
    for(auto& y:x) {
      cout << y << " ";;
    }
    cout << endl;
  }

  
  return 0;
}

// printing 
  2 4 6 
  3 5 7
  
```

---

## Matrix Operation
### Matrix Addition

```cpp
#include <iostream>
using namespace std;

int main()
{
  int A[2][3] = {3, 3, 3, 3, 3, 3}; 
  int B[2][3] = {1, 1, 1, 1, 1, 1};
  int C[2][3];

  // Adding A & B and string into C
  for(int i = 0; i < 2; i++) {
    for(int j = 0; j < 3; j++) {
      C[i][j] = A[i][j] + B[i][j];
    }
  }

  // print added new Array
  for (int i = 0; i < 2; i++) {
    for (int j = 0; j < 3; j++) {
      cout << C[i][j] << " ";
    }
    cout <<endl;
  }

  
  return 0;
}

```


### Matrix Subtraction

```cpp
#include <iostream>
using namespace std;

int main()
{
  int A[2][3] = {3, 3, 3, 3, 3, 3}; 
  int B[2][3] = {1, 1, 1, 1, 1, 1};
  int C[2][3];

  // Subtracting A & B and string into C
  for(int i = 0; i < 2; i++) {
    for(int j = 0; j < 3; j++) {
      C[i][j] = A[i][j] - B[i][j];
    }
  }

  // print Subtracted new Array
  for (int i = 0; i < 2; i++) {
    for (int j = 0; j < 3; j++) {
      cout << C[i][j] << " ";
    }
    cout <<endl;
  }

  
  return 0;
}

```

---

## Write a Program to Calculate Average of all element in an Array.

```cpp
#include <iostream>
using namespace std;
int main(){
  int n, i;
  float num[100], sum=0.0, average;
  cout << "Enter the numbers of elements: ";
  cin >> n;
  for(i = 0; i < n; ++i) {
    cout << i + 1 << ". Enter number: ";
    cin >> num[i];
    sum += num[i];   
  }   
  average = sum / n;
  cout << "Average = " << average;
  return0;
} 
```

## Program to Multiplication of two Array


---



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