# bigint-library
C++ Library for Large Integers  

## Idea for Creation
This is a C++ library for large integers. I made this C++ code library because there are no built-in large integers library (like BigInteger in Java) in C++.  
In this version, **integer is restricted to be non-negative.** We will add some features because it is still in development. Though, you still can use this version because it supports addition, subtraction, and multiplication, and even division!  

In this implementation, arithmetic operations especially for multiplication and division **run in a rapid time complexities**!  

* Addition: O(n) time complexity  
* Subtraction: O(n) time complexity  
* Multiplication: O(n log n) time complexity  
* Division: O(n log n) time complexity, about 10x slower than multiplication  

## How to use?
The class name of this library is "bigint".  
In order to use "bigint", we need to include "bigint.h" in your source code.  

The example of code is like this:  
~~~
#include "bigint.h"
int main() {
	bigint x = 13, y = 8;
	std::cout << x + y << '\n'; // outputs 21
	std::cout << x - y << '\n'; // outputs 5
	std::cout << x * y << '\n'; // outputs 104
	return 0;
}
~~~

## Basic Implementation / Functions

### Implementation
It stores numbers as a 10<sup>4</sup>-ary number. In this implementation, the number of digits can be represented as <sup>2^n</sup>, because doing this makes implementation easier (and it is convenient to do FFT)
In this library, we can hold up to 2<sup>27</sup> digits in decimal (in 10<sup>4</sup>-ary number, it is 2<sup>25</sup> digits).  
So, the range of bigint x is, 0 ≤ x < 10<sup>2<sup>27</sup></sup>.  
