# Week03 Quiz2:

<br/>

## 1. Requirements:

A number that can be expressed as a ratio `(x/y)` of two integers is called a rational number (the denominator should not be zero). We want to define rational numbers by a class. Make a program with C++ which have following functions:  

1. When the user enters the numerator and denominator of two rational numbers, Rational objects `a` and `b` are created.  

2. Converting these objects into four arithmetic operations `(+, -, *, /)` and the result is stored in the new Rational object.   

3. The operation result is always stored as a irreducible fraction.  

4. Convert rational numbers to double types while keeping two decimal places.  

*irreducible fraction: 1 is the unique common divisor of the numerator and denominator. `e.g. 2/3, 3/7 ` 

### Input  

- The first line inputs `two numbers (int type)` separate by space, representing the numerator and denominator of the first rational number `a`.(The second line will output its irreducible fraction result.)  
`e.g. 3 9`
- The third line inputs `two numbers (int type)` separate by space, representing the numerator and denominator of the second rational number `b`.(The fourth line will output its irreducible fraction result.)  
`e.g. 2 -20`  

### Output

- The second line and the fourth line will output irreducible fraction results of `a` and `b`, there should be no spaces between numbers and symbols.     
`e.g. -1/3`
- The next four lines output the arithmetic equations and results for operations `a` and `b`, separating each item from the operator with a space.     
`Format: a + b = c (rational form) = d (double type with two decimal places retained)`.

### Precautions:
• If the denominator is negative, the numerator is converted to negative and the denominator is converted to positive and stored   
`e.g. (1/-3 -> -1/3)`.  

• If both the numerator and denominator are negative, both the numerator and denominator are converted to positive and stored   
`e.g. (-1/-3 -> 1/3)`.  

• Fractions with a numerator of 0 and a denominator of n are stored as a reduced fraction of 0/1   
`e.g. (0/3 -> 0/1)`.  

• If the denominator is zero, the program should throw an error and require a new input.
`e.g. (3/0 -> "Error: Denominator can't be zero. Please input numerator and denominator again.")`.

• If the numerator is a multiple of the denominator and is converted to an integer, it is stored as a fraction with a denominator of 1   
`e.g. (6/3 -> 2/1)`  

• Methods that output retain two decimal places:  `cout << ... << setprecision(2) << fixed << d << endl;`  

• Requires <sstream> inclusion to use ostringstream class  

• Assume that the denominator of the rational number input by the user and the denominator of the rational number of the calculation result are not zero.  

<br/>
<br/>

## 2. Scoring Criteria (Total 5 points):

- No compile errors: 1 point
- The zero exception handling is implement: 2 point
- The output of the calculate results are correct: 2 point

<br/>
<br/>

## 3. Examples: 

### Example1 (Red font for input, blue font for output):

![image](https://github.com/chyh001228/images/blob/main/w3q2.png)  

**Input:**
```
3 0
3 9
2 -20
```
  
**Output:**
```
Error: Denominator can't be zero. Please input numerator and denominator again.
1/3
-1/10
1/3 + -1/10 = 7/30 = 0.23
1/3 - -1/10 = 13/30 = 0.43
1/3 * -1/10 = -1/30 = -0.03
1/3 / -1/10 = -10/3 = -3.33
```

**Actual results:**  
![image](https://github.com/chyh001228/images/blob/main/w3q2_c.png) 

<br/>

### Example2 (Red font for input, blue font for output):

![image](https://github.com/chyh001228/images/blob/main/w3q2_e2.png)  

**Input:**
```
5 -10
3 0
3 7
```
  
**Output:**
```
-1/2
Error: Denominator can't be zero. Please input numerator and denominator again.
3/7
-1/2 + 3/7 = -1/14 = -0.07
-1/2 - 3/7 = -13/14 = -0.93
-1/2 * 3/7 = -3/14 = -0.21
-1/2 / 3/7 = -7/6 = -1.17
```

**Actual results:**  
![image](https://github.com/chyh001228/images/blob/main/w3q2_c_e2.png) 

<br/>

### Example3 (Red font for input, blue font for output):

![image](https://github.com/chyh001228/images/blob/main/w3q2_e3.png)  

**Input:**
```
6 -9
-3 2
```
  
**Output:**
```
-2/3
-3/2
-2/3 + -3/2 = -13/6 = -2.17
-2/3 - -3/2 = 5/6 = 0.83
-2/3 * -3/2 = 1/1 = 1.00
-2/3 / -3/2 = 4/9 = 0.44
```

**Actual results:**  
![image](https://github.com/chyh001228/images/blob/main/w3q2_c_e3.png) 

<br/>

<img src="https://cdn.imweb.me/upload/S201906178853c3e170808/c5d876d707352.jpg" width=30% align=center />
