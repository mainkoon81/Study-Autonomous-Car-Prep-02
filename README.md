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
This function takes in a velocity and time. These are multiplied together to calculate a distance. 
<img src="https://user-images.githubusercontent.com/31917400/43330645-bc088dd0-91bb-11e8-9a5a-bc71d111f1c5.jpg" />

























