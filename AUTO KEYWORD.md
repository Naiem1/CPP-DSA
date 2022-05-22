## `auto` keyword
  > `auto` keyword is used for **variable declaration**

> If we use *`auto`* we do not have to type the exact data type like `int`, `float`, `char` etc. We just have assign a value and compiler will automatically infer the data type of certain variable.

***Example code:***

```C++
#include <iostream>
#include <typeinfo>
using namespace std;

int main() {
   auto a = 10; // here I used auto before a.
   auto b = 15.5; // I have used auto before b and I assign a floating point value compiler automatically infer to data type for b.
   auto c = 'A';
   auto s = "Hello world!";
   auto boo = true;

   cout << a << endl; // 10
   cout << b << endl; //  15.5
   cout << c << endl; // 'A'
   cout << s << endl; // Hello World
   cout << boo << endl; // true

  /* After that to check what datatype I have been assign to all the variable better understanding the `auto` 
  I have used typeid(variable).name. whe we pass variable into typeid it give the type info of that variable and .name gives us short name of data type */
	
   cout << typeid(a).name() << "\n"; // i
   cout << typeid(b).name() << "\n"; // d
   cout << typeid(c).name() << "\n"; // c
   cout << typeid(s).name() << "\n"; // Pkc
   cout << typeid(boo).name() << "\n"; // b

   return 0;
}
```

>  After that to check what datatype I have been assign to all the variable better understanding the `auto` I have used `typeid(variable).name` when we pass variable into `typeid` it give the type info of that variable and `.name` gives us short name of data type

***Note:*** float assign a **double**. the constant we used in out program it called ***Literal***. Literal have there default datatype. `int` datatype by default treat as `int` not not `long long` or `long` etc. but `floating` point treat as `double`

## Advantages of auto keyword
1. No conversion happens when auto is used
   - whe we create a variable with auto keyword and assigned **literal** to it no conversion happens, because literal have there own default types
    ```cpp 
      float x = 3.4; // double literal converted to float, but here conversion happens because value is double type and variable is float
      auto y = 3.4 // type of y is double. value is double type so y is automatically becomes double
    ```
2. If a function return `auto`, its return type can be change without worrying about prototype change.
  - function has a declaration and they have definition also, and declaration typically happen in the header file now function declaration contain `auto` we can change function return anytime without change the type of function declaration.

3. Can be very helpful for lengthy types, especially `STL` iterations. 
    ```cpp
      vector<int>:: iterator i;
      // can be replaced with
      auto i;
    ```

4. Lambda Expression
   - Something where `auto` is must. we can assign a lambda express to a variable. Type of a lambda express only known to to the compiler. we don not know type of a lambda express as a programmer so we have to use `auto`.
   - **What is lambda Expression:-**  Lambda express are anonymous function. create a function with out give any name

if we use to much `auto` everywhere it reduce readability of the program. we can not figure out what is the data type.

---
