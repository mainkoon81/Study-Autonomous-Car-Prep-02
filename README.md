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
A C++ functions consists of a function **declaration** and a function **definition**. Because C++ is statically typed, you need to specify the data types for the function input variables and the data type of whatever the function returns. 
<img src="https://user-images.githubusercontent.com/31917400/43340999-14442940-91d6-11e8-9f01-df132adc293c.jpg" />

This function takes in a velocity and time. These are multiplied together to calculate a distance. 
<img src="https://user-images.githubusercontent.com/31917400/43341711-3c3b3248-91d8-11e8-8649-10fde9952f70.jpg" />

> In C++, functions can only have one output. 
> We can make up a type. What if we need **lists of floats** within a list? In C++, they are vectors of floats within a vector and called `vector < vector <float> >`. Let's call it 't_grid'.   
```
typedef vector < vector <float> > t_grid;
```
> Sometimes we could have two different functions which each had the same name and this didn't cause any problems. This is because in C++, the function name is not the signature. The return value, type, inputs, etc constitute the signature.    
<img src="https://user-images.githubusercontent.com/31917400/43343226-6d99ac0c-91dd-11e8-86b6-0b495864b533.jpg" />
<img src="https://user-images.githubusercontent.com/31917400/43343414-f9bc5806-91dd-11e8-937e-a30494e9cb39.jpg" />

The signature for the normalize function is:
```
vector< vector<float> > normalize(vector< vector <float> > grid);
```
























