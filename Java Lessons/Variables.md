# Variables

## Like in Algebra variables like x, y, etc. stores values

### How variables are used in math:

```
x = 5
y = x / 2

The value of y is 2.5
```

### How variables are used in programming:

```java
// The layout of making variables
datatype variableName = value

// Variable names have to start with letters not numbers, but you can use numbers after letters.

// datatype    // variableName   // value
int            x               = 5;
int y = x / 2; // The value of y is 2.5

double pi = 3.14159;

boolean running = false;

char letterA = 'a'

String sentence = "This is a sentence"

// If you know what values (they are set) will be inside the array you can make an array like so:

int[] integerArray = {1, 2, 3, 4, x, y}; //Since x and y are both integers they can be apart of the integer array

// If you do not know what will be going inside the array you can make an array like so: 

double[] doubleArray = new double[6]; // Making a new double array with the size of 6 (There can only be 6 values in the array)
double[0] = 1.0; // In the zeroth index store the value 1.0 (Computers start counting from zero)
double[1] = 2.0; // The second value but the first index
double[2] = 3.0;
double[3] = 4.0;
double[4] = 5.0;
double[5] = pi; // Since pi is a double it can be stored in the array
```

> So if later on we want to get the value of a variable later we would just reference it by the variable name you put.

## Assignment

* Make your own variables with all the different data types.
* Make an integer array that **can** store 8 values
    * Set the second value in the array to 100.
    * Set the seventh index in the array to 1000.
    * Fill the rest of the array with any numbers
* Make your own array with any data type with **set values**