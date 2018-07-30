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

**1> empty vectors**

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
**2> Namespaces**

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

**3> filling up a vactor**

To initialize vector values, 
<img src="https://user-images.githubusercontent.com/31917400/43357501-a20b685c-927a-11e8-9c51-757c3892962b.jpg" />

But there are various other ways for assigning initial values to a vector. For example,
 - When declaring a vector, you can also assign initial values simultaneously: 
   - `std::vector<int> myvector(10, 6);` It will declare a vector with ten elements, and each element will have the value 6.
 - If you are using one of the more recent versions of C++, 
   - `std::vector<float> myvector = {5.0, 3.0, 2.7, 8.2, 7.9};`  

**4> useful vector methods**(for the object oriented programming)
 - `variable.assign(10,16);`: It'll populate the vector with ten integers all having the value of 16. 
   - It seems not differ from `std::vector<int> variable(10,16);` in the beginning, but the difference is that the `.assign()`method lets you **override** current vector with new values.
 - `variable.push_back(25);`: I'll adds(appends) an element'25' to the end of the vector. 

**5> vectors & for-loop**
 - Much of the time, you will be using for loops to manipulate vectors.
   - populate a vector with values
   - do math with vectors

For example, initializes a vector and then uses a for loop to **populate** the vector with values. Then another for loop **reads out** the vector values: 
 - 0 
 - 5.231 
 - 10.462 
 - 15.693 
 - 20.924
```
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<float> example;
    
    for (int i = 0; i < 5; i++) {
        example.push_back(i * 5.231);
    }
    for (int i = 0; i < example.size(); i++) {
        cout << example[i] << endl;
    }
    return 0;
}
```
 - // Declare and define a vector {5.0, 5.0, 5.0}, // Print it out
 - // Use **push back** to add the values 3.0, 2.5, 1.4 to the back of the vector, // Print out the vector
 - // Use the **assign** method so that the current vector has values {5.0, 5.0, 5.0}, // Print out the vector
```
int main() {

    vector<float> vectorvar(3, 5.0);
    for (int i = 0; i < vectorvar.size(); i++) {
        cout << vectorvar[i] << " ";
    }
    cout << endl;
    
    
    vectorvar.push_back(3.0);
    vectorvar.push_back(2.5);
    vectorvar.push_back(1.4);
    for (int i = 0; i < vectorvar.size(); i++) {
        cout << vectorvar[i] << " ";
    }
    cout << "\n";
    
    
    vectorvar.assign(3, 5.0);
    for (int i = 0; i < vectorvar.size(); i++) {
        cout << vectorvar[i] << " ";
    }
    cout << "\n";

    return 0;
}
```
`i++` VS `++i`: In practice, both i++ and ++i will give you the same results; these are a shorthand way of writing i = i + 1. The difference between the two is subtle: 
```
int i = 5;
int x = i++;   // x = 5, i = 6 (called postfix)
int x = ++i;   // x = 6, i = 6 (called prefix)
```
 - In the postfix case, `i++`, `int x = i` is evaluated first and then `i = i + 1` occurs.
 - In the prefix case, `++i`, `i = i + 1` occurs first and then `int x = i` executes
> When overloading the postfix operator, C++ needs to keep track of two values. In the example, the values would be 5 and 6. For the prefix operator, C++ only needs to keep track of one value: 6. Hence, when overloading the ++ operator, it's generally more efficient to use prefix than the postfix.
```
class A
{
public:
    A & operator++();   //Prefix (++i)
    A operator++(int);  //Postfix (i++)
}
```
**math example**
 - multiply every element in a vector
 - add two vectors together
<img src="https://user-images.githubusercontent.com/31917400/43360192-f5e775a0-92a8-11e8-9e49-d42f9fdc5304.jpg" />

> **1D vector math**
 - Initialize a vector with the values [17,10,31,5,7]. Initialize another vector with the values [3,1,6,19,8]. Then, output another vector that contains the product of each element. In other words, the vector should have [17×3, 10×1, 31×6, 5×19, 7×8].
```
#include <iostream>
#include <vector>
using namespace std;

// **function declaration
vector<float> product(vector<float> vector1, vector<float> vector2);

// program that computes the element-wise multiplication of two vectors
int main() {
	vector<float> v1(5);
	vector<float> v2(5);
	v1[0] = 17.0;
	v1[1] = 10.0;
	v1[2] = 31.0;
	v1[3] = 5.0;
	v1[4] = 7.0;
	v2[0] = 3.0;
	v2[1] = 1.0;
	v2[2] = 6.0;
	v2[3] = 19.0;
	v2[4] = 8.0;
	
	// declare and initialize a result vector
	vector<float> v3(v1.size());
	// calculate the difference between the two vectors
	v3 = product(v1, v2);
	// print out the results of the vector multiplication
	for (int i = 0; i < v3.size(); i++) {
		cout << v3[i] << " ";
	}
	cout << endl;
	
	return 0;
}

// **function definition
vector<float> product(vector<float> vector1, vector<float> vector2) {

	vector<float> result(vector1.size());

	for (int i = 0; i < vector1.size(); i++) {
		result[i] = vector1[i] * vector2[i];
	}
	return result;
}
```
> **2D vector math**
 - Much like how Python uses a list of lists to store matrices, for the C++, we use a vector of vectors. How to declare two-dimensional vectors?  
<img src="https://user-images.githubusercontent.com/31917400/43361075-d5405262-92bd-11e8-80cb-2d47d61d5340.jpg" />

> Here is another way you could have set up the vector from the previous example:
 - The syntax is a little bit more complicated. But if you start from the inside of the parenthesis and work your way out, you see that you have already seen all of the functionality. 
 - `vector<int> (3, 2)` would set up an integer vector like {2, 2, 2}. So even though you don't see the inner vector, the code is essentially doing something like this:`vector < vector<int> > twodvector (5, {2, 2, 2});`.
 - only Python represents vectors or matrices with square brackets `[]`. Newer versions of C++ can use squiggly brackets to represent vectors `{}`.
```
vector < vector<int> > twodvector (5, vector<int> (3, 2));
```
Write a function that has two integer(5x3)matrices as inputs and then outputs the sum. Assume that the two input matrices have the same size.
```
#include <iostream>
#include <vector>
using namespace std;

vector < vector<int> > matrixsum(vector < vector<int> > matrix1, vector < vector<int> > matrix2);
void matrixprint(vector < vector<int> > inputmatrix);

int main() {

	// declare two matrices
	vector < vector <int> > matrix1 (5, vector <int> (3, 2));
	vector < vector <int> > matrix2 (5, vector <int> (3, 26));

	//declare an empty matrix to hold the result
	vector < vector <int> > matrixresult; 

	//calculate the sum of the two matrices
	matrixresult = matrixsum(matrix1, matrix2);

	// call the matrix print function to print out the results
	matrixprint(matrixresult);

	return 0;
}

//function to add two matrices together
vector < vector<int> > matrixsum(vector < vector<int> > matrix1, vector < vector<int> > matrix2) {

	// declare a matrix with the same size as matrix1 and matrix2
	vector < vector<int> > matrixsumresult (matrix1.size(), vector<int> (matrix1[0].size(), 0));

	// iterate through matrix1 and assign the sum of each element to the results matrix
	for (int row = 0; row < matrix1.size(); row++) {
		for (int column = 0; column < matrix1[0].size(); column++) {
			matrixsumresult[row][column] = matrix1[row][column] + matrix2[row][column];
		}
	}
	return matrixsumresult;
}

// function to print an integer matrix
void matrixprint(vector < vector<int> > inputmatrix) {

	for (int row = 0; row < inputmatrix.size(); row++) {
		for (int column = 0; column < inputmatrix[0].size(); column++) {
			cout << inputmatrix[row][column] << " ";
		}
		cout << endl;
	}
}
```

### [Standard Library]
> **making our terminal to ask us to input** 

We know how to call a function and then **output** the results to the terminal using `cout`. But how do you **get user input** from the terminal? Or how do you input **data from a file** into your program or write out your results to a file? 
 - Much like the **Standard Library** provides a function for outputting to the terminal, it also provides a function for reading in data from the terminal: `cin` (c-out vs c-in)..so this makes our shell terminal to ask us to input sth.    
```
#include <iostream>
#include <vector>
using namespace std;

int main() {

    int integerone; 
    int integertwo;

    // declare array and assign values
    cout << "Enter an integer between 1 and 100" << endl;
    cin >> integerone;

    cout << "Enter another integer between 1 and 100" << endl;
    cin >> integertwo;

    // output the difference
    cout << "The difference between your two numbers is: ";
    cout << integerone - integertwo << endl;
    return 0;
}
```
> **outputting to our terminal display**

The **Standard Library** includes functionality for reading text files line by line. You can then parse each line of the text file one line at a time. Say, for example, you have a text file with numbers and commas representing a 3 by 4 matrix:
```
1, 6, 2, 10.5
11, 15.2, 2, 21
3, 9, 1, 7.5
```
You want to read in this file and create a 2D vector to represent the matrix. Then the code outputs the matrix to the terminal display. 
```
#include <iostream>
/fstream provides functions and classes for reading in and outputting files.
#include <fstream>
/The sstream file in the Standard Library provides functionality for manipulating and parsing the string. 
#include <sstream>
#include <string>
#include <vector>
using namespace std;

int main() {

    // initialize string variables for reading in text file lines 
    string line;
    // first a sstream object is declared and then later the "ss" object is used to cycle through and parse each line of the text file:
    stringstream ss;

    // initialize variables to hold the matrix
    vector < vector <float> > matrix;
    vector<float> row;

    // counter for characters in a text file line
    float i;

    // read in the file
    // This line of code reads in the file "matrix.txt" and then creates an object called "matrixfile" that you can use for reading in the text file...
    ifstream matrixfile ("matrix.txt");

    // read in the matrix file line by line
    // parse the file..The if statement that follows checks that the file opened correctly.
    // and then a while loop reads the file one line at a time. Each line is placed into a variable called "line".

    if (matrixfile.is_open()) {
        while (getline (matrixfile, line)) {

            // parse the text line with a stringstream
            // clear the string stream to hold the next line
            ss.clear();
            ss.str("");
            ss.str(line);
            row.clear();

            // parse each line and push to the end of the row vector
            // the ss variable holds a line of text
            // ss >> i puts the next character into the i variable. 
            // the >> syntax is like cin >> some_value or cout << some_value
            // ss >> i is false when the end of the line is reached
	    // the code finds a float number and appends the number to the vector called row. 
	    // The line "ss.peek()" looks at the next character to see if it is a comma or a space and ignores commas or spaces.

            while(ss >> i) {
                row.push_back(i);

                if (ss.peek() == ',' || ss.peek() == ' ') {
                    ss.ignore();
                }
            }

            // push the row to the end of the matrix
            matrix.push_back(row);
        }
	// when you are done with reading in the file, it's a good habit to close the file, otherwise our program could crash.
        matrixfile.close();

        // print out the matrix
        for (int row = 0; row < matrix.size(); row++) {
            for (int column = 0; column < matrix[row].size(); column++) {
                cout << matrix[row][column] << " " ;
            }
            cout << endl; 
        }
    }

    else cout << "Unable to open file";

    return 0;
}
```
> **outputting to textfiles**

We can also output data to a file. Say you have a matrix and you want to save the results to a text file. 
 - you need to create an ofstream object and then use the object to create a new file.
```
#include <iostream>
#include <fstream>
#include <vector>
using namespace std;

int main() {
    // create the vector that will be outputted
    vector< vector<int> > matrix(5, vector<int>(3,2));
    vector<int> row;
    
    // open a file for outputting the matrix (in User's folder..declaring its location?)
    ofstream outputfile;
    outputfile.open("matrixoutput.txt");
    
    // output the matrix to the textfile
    if(outputfile.is_open()) {
       for(int row=0; row < matrix.size(); row++) {
          for(int col=0; col < matrix[row].size; col++) {
	     // Here, the if statement is checking whether or not 'the end of the row' is reached.
	     if(col != matrix[row].size() -1) {
	        outputfile << matrix[row][col] << ", ";
	     } 
	     else {
	         outputfile << matrix[row][col];
	     }
	  }
	  outputfile << endl;
       }
    }
    outputfile.close();
    return 0;
}
```
## C++ object oriented Coding
Object-oriented programming has the advantage of being **modular** and **testable** by making good separation b/w one piece of code or another. In SelfDCar, a wheel class, a sensor class for seeing where the lanes are, a camera class used from other people, etc...we'd end up with a huge complicated system, but if everything is self-contained, very individual, objecty, encapsulated into its own separate thing, then as you change the wheels to different wheels, we can just swap that out!!!
## Class
 - Ex> 'Gaussian': This class stores the values for the standard deviation and mean. The class also has methods for calculating the probability density function, the sum of two gaussians, and the product of two gaussians. The class contains two class variables called `mu`, `sigma2`.
<img src="https://user-images.githubusercontent.com/31917400/43409347-97b867c2-941b-11e8-95d5-acfb1309737b.jpg" />

 - Unlike Python, in C++, all of its **variables** and all of its **functions** need to be declared first before writing the implementation. 
 - The class also has a part labeled **private** and another part labeled **public**. 
 - Furthermore, the C++ class includes **extra functions** like `setMu`, `setSigma2`, `getMu`, and `getSigma2`.
<img src="https://user-images.githubusercontent.com/31917400/43410091-abc1b4c4-941d-11e8-9d28-3dde43aff2bf.jpg" />
 
 - In C++, you might not want a program to have direct access to certain variables. The `set..()` functions allow a program to change the values in those variables without getting direct access to them. 

> **main.cpp** and **gaussian.cpp** How they work together?
 - The main.cpp file: 
   - It **uses the class** to run some calculations. You'll see one important difference between C++ and Python. In C++, you need to declare your class before you can use the class. Both main.cpp and gaussian.cpp have the same class declaration at the top of their files. In short, the **main.cpp** used the Gaussian class.
 - The gaussian.cpp file: 
   - It contains the **class definition** including all the variables and functions that the Gaussian class needs. In short, the **gaussian.cpp** contained the code that defined the Gaussian class. 

This is `main.cpp` file. You can't see it on the backend, but this program is first being compiled via the command: `g++ main.cpp gaussian.cpp`. 
```
#include <iostream>

//class declaration
class Gaussian {
    private:
        float mu, sigma2;
	
    public:
        //constructor functions
	Gaussian();
	Gaussian(float, float);
	
	//change values
	void setMu(float);
	void setSigma2(float);
	
	//output values
	float getMu();
	float getSigma2();
	
	//functions to evaluate
	float evaluate(float);
	Gaussian mul(Gaussian);
	Gaussian add(Gaussian);
};

int main() {
    Gaussian mygaussian(30.0,100.0);
    Gaussian othergaussian(10.0,25.0);
    std::cout << "average " << mygaussian.getMu() << std::endl;
    std::cout << "evaluation " << mygaussian.evaluate(15.0) << std::endl;
    std::cout << "mul results variance " << mygaussian.mul(othergaussian).getSigma2() << std::endl;
    std::cout << "mul results average " << mygaussian.mul(othergaussian).getMu() << std::endl;
    std::cout << "add results variance " << mygaussian.add(othergaussian).getSigma2() << std::endl;
    std::cout << "add results average " << mygaussian.add(othergaussian).getMu() << std::endl;
    return 0; 
}
```
It outputs..
```
average 30
evaluation 0.0700165
mul results variance 20
mul results average 14
add results variance 125
add results average 40
```
 - The main.cpp file had three parts:
   - a header, which is where the #include statements were
   - a class declaration
   - a main function.

> header
 - The header included the library for outputting to the terminal: `#include <iostream>`. 
> class declaration
 - Then comes the class declaration. In fact, you can put the class declaration into a separate `blahblah.h` file just like we did with function declarations. The purpose of the class declaration is to give the main function access to the Gaussian class. Notice that a class declaration looks a lot like the variable declarations and function declarations we've already been using. Declarations tell the program what the variable types will be. The declarations also show the input and output types for functions.
> main function
 - And finally comes the main function. The main function instantiates objects of the Gaussian class. So the main function uses the class whereas gaussian.cpp defined the class. You could take the code in gaussian.cpp and put it at the bottom of main.cpp; however, your code files will become quite large and hard to read through.



 
 

















































































