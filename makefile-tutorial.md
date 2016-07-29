#Unix Makefile Tutorial
Makefile is a program building tool which runs on Unix, Linux, and their flavors. It aids in simplifying building program executables that may need various modules. To determine how the modules need to be compiled or recompiled together, make takes the help of user-defined makefiles.


##Prerequisites
This tutorial expects good understanding of programming language such as C and C++. The reader is expected to have knowledge of linking, loading concepts, and how to compile and execute programs in Unix/Linux environment.

##Why do we need Makefile?
Compiling the source code files can be tiring, especially when you have to include several source files and type the compiling command every time you need to compile. Makefiles are the solution to simplify this task.
For example, let’s assume we have the following source files.
* main.cpp
* hello.cpp
* factorial.cpp
* functions.h

###main.cpp
```c++
#include <iostream>

using namespace std;

#include "functions.h"

int main(){
   print_hello();
   cout << endl;
   cout << "The factorial of 5 is " << factorial(5) << endl;
   return 0;
}
```
###hello.cpp
```c++
#include <iostream>

using namespace std;

#include "functions.h"

void print_hello(){
   cout << "Hello World!";
}
```
###factorial.cpp
```c++
#include "functions.h"

int factorial(int n){
   
   if(n!=1){
      return(n * factorial(n-1));
   }
   else return 1;
}
```
###functions.h
```c++
void print_hello();
int factorial(int n);
```
