# Study-SelfDCar-Prep
Self Driving Car Preparation

--------------------------------------------------------------------------------
### Intro to C++

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

## Control Statements
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

















