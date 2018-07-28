# Study-SelfDCar-Prep
Self Driving Car Preparation

--------------------------------------------------------------------------------
## Intro to C++

Let's see "5 + 9", "12.07 + 65.102". Note `std::endl` or `'\n'` let the result show up all the time. 
```
// include all libraries needed
// The definition of 'std' is in the 'iostream file' of the standard library, which needs to be included at the top of the program with the line "#include <iostream>". Otherwise, your program won't recognize what 'std' means.

/* 	
* These are C++ comments. There are two ways to write comments in C++.
* Using the slash with an asterisk is one way.
*/ 

// Here is another way to write comments in C++

/* In general, C++ code is run from a file called main.cpp
* The implementation goes into a function called main().
* The main() function almost always returns a zero, which provides evidence that the program ran to its end.
*/

// define main function
// Define a variable called integer_two and assign a value of 9.
// Calculate the sum of integer_one and integer_two and assign the result to integer_sum
// outputs the results to standard out

#include <iostream>
int main() {
    int integer_one;
    integer_one = 5;
    int integer_two;
    integer_two = 9;
    int integer_sum;
    integer_sum = integer_one + integer_two;
    std::cout << integer_sum << std::endl;
    
    float first_fl = 12.07;
    float second_fl = 65.102;
    float float_sum;
    float_sum = first_fl + second_fl;
    std::cout << float_sum << std::endl;

    return 0;
}
```
> C++ function consists of a function **declaration** and a function **definition**. Because C++ is statically typed, you need to specify the data types for the function input variables and the data type of whatever the function returns. 
<img src="https://user-images.githubusercontent.com/31917400/43340999-14442940-91d6-11e8-9f01-df132adc293c.jpg" />

> This function takes in a velocity and time. These are multiplied together to calculate a distance. In C++, functions can only have one output. 
<img src="https://user-images.githubusercontent.com/31917400/43341711-3c3b3248-91d8-11e8-8649-10fde9952f70.jpg" />

> We can make up a type. What if we need **lists of floats** within a list? In C++, they are vectors of floats within a vector and called `vector < vector <float> >`. Let's call it 't_grid'.   
```
typedef vector < vector <float> > t_grid;
```
> Sometimes we could have two different functions which each had the same name and this didn't cause any problems. This is because in C++, the function name is not the signature. The return value, type, inputs, etc constitute the signature.    
<img src="https://user-images.githubusercontent.com/31917400/43343226-6d99ac0c-91dd-11e8-86b6-0b495864b533.jpg" />
<img src="https://user-images.githubusercontent.com/31917400/43343414-f9bc5806-91dd-11e8-937e-a30494e9cb39.jpg" />

> The signature for the normalize function is:
```
vector< vector<float> > normalize(vector< vector <float> > grid);
```

### [Control Statements]
**if statements** and the associated boolean logic.
<img src="https://user-images.githubusercontent.com/31917400/43347064-ba2ee13c-91eb-11e8-8b29-2408e6e3a446.jpg" />

**while loop** 
<img src="https://user-images.githubusercontent.com/31917400/43347776-b771d258-91ee-11e8-8722-54c80b2fb8ef.jpg" />

**for loop**
<img src="https://user-images.githubusercontent.com/31917400/43347839-f9a164c2-91ee-11e8-936e-b1058e3ffcf6.jpg" />

For python the iterator was defined here, and generates a list of numbers `[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14]`.
```
for i in range(0, elapsed_time):
```
For C++, the generation happens in this..First you declare the variable `i` and assigned a value (in this case zero). 
```
for (int i = 0; i < elapsed_time; i++) {
```
The for loop then checks if `i < elapsed_time`. If **true**, then the code block is run and then `i` **increases by one**. The code `i++` is equivalent to saying **i=i+1**. When `i=14` that will be the last time that the code block runs. The code checks that 14 is less than 15, runs the code block and increases `i` to 15. Then the code checks if 15 is less than 15. Since that is **false**, the for loop does not run again.

**switch statement**

A switch statement is very similar to an if clause. In fact, you can write a program that does the exact same thing with either a switch statement or a series of if-else clauses. Then why bother using a switch statement? switch statements can oftentimes be faster to execute. Many programming languages have a switch statement including Java. 
<img src="https://user-images.githubusercontent.com/31917400/43350339-482b14a8-91fe-11e8-85cd-782dd8c775c7.jpg" />

The output of the code would be
```
Not Moving - Neutral
Your car is currently in gear: N
```
> **Switch Limitations**: 

If-else statements are much more flexible than switch statements. In fact, the **case clauses** in switch statements can only make **comparisons** between **integer** values, between **characters** because C++ is actually converting the characters to integers. On the other hand, **if statements** can make comparisons between floating point numbers as well as between integers. 

> **Standard Library**:

What if you want to store a string in a variable or do more advanced math like taking the square root of a number? Just like Python, C++ also uses pre-built libraries to help make programming easier: The **C++ Standard Library** has a lot of functions and classes like a definition for a string, arrays, tuples, functions **for reading** in and **outputting** files, **random number generators**, **definitions for complex number variables**, **mathematical functions** and many other functions as well. https://en.cppreference.com/w/cpp/header
```
#include <iostream>
#include "distance.h"
```
In general, **<>** directs the program to look for system headers in a specific folder. The double quotes **" "** tell the program to look for the header files in the same directory as the **main.cpp file**. but using quotes instead of brackets is less efficient. When using quotes, your program will first look for the iostream file in the main.cpp directory. When the program cannot find the file, the program will search where the standard library files are kept. Aside from Standard Library, there are many other useful C++ libraries that you install separately. Each library will have its own installation procedure and usually comes with instructions. https://en.cppreference.com/w/cpp/links/libs

### [Vectors]
When you were writing Python programs to store and manipulate matrices, you used Python lists. C++ vectors are just like Python lists.
But hold on! C++ also has something called a list. But this is where things get confusing. However, C++ lists do not work the same way as Python lists. C++ lists and C++ vectors are both in a family of structures called **sequence containers**. These containers allow you to store values in series and then access those values. C++ has a handful of sequence containers including **lists**, **vectors**, and **arrays**. 

**empty vectors**

The vector type definition has a funny looking syntax because you also need to **declare** what kind of values will go inside the **vector** such as int, char, float, string, etc....for an example of declaring an empty vectors...
```
#include <vector>

int main () {
    std::vector<char> vector_name1;
    std::vector<int> vector_name2;
    std::vector<float> vector_name3;
    return 0;
}
```
**Namespaces**

C++ vector syntax is a little bit hard to read because you have to type `std` over and over again: like for example, `std::cout` or `std::string` or `std::vector`. Thankfully, C++ provides a way to avoid writing `std` all the time. `std` is something called a **namespace**. Without getting too much into the details, namespaces let you organize code into logical groups. In this case, `std` is the namespace for the Standard Library. `using namespace std;`. For example,...note `cout`, `endl`.
```
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> vector_1;
    int intvariable = 5;
    cout << intvariable << endl;
    return 0;

} // what the fuck vector_1 is empty ???
```
> Declaring the namespace makes the code easier to read and write. The downside is that you have to be careful with how you name your own variables and functions. 
> - Namespaces help group related code together.
> - Namespaces help avoid conflicts b/w variable, function, class names  
> - Declaring a namespace in our program's header, allows to avoid writing out the namespace name multiple times in our code. 

**filling up a vactor**

To initialize vector values, 
<img src="https://user-images.githubusercontent.com/31917400/43357501-a20b685c-927a-11e8-9c51-757c3892962b.jpg" />

But there are various other ways for assigning initial values to a vector. For example,
 - When declaring a vector, you can also assign initial values simultaneously: `std::vector<int> myvector(10, 6);` It will declare a vector with ten elements, and each element will have the value 6.
 - If you are using one of the more recent versions of C++, `std::vector<float> myvector = {5.0, 3.0, 2.7, 8.2, 7.9}`  

**vector methods**(Useful functions for the object oriented programming)
 - `vector<int> variable; variable.assign(10,16);`: It'll populate the vector with ten integers all having the value of 16. It seems not differ from `vector<int> variable(10,16);` but the difference is that the `.assign()`method lets you override your current vector with new values.
 - `vector<int> variable; variable.push_back(25);`: I'll adds(appends) an element'25' to the end of the vector. 












