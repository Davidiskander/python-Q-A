### Task 1 (If-else Statement)
Given an integer, , perform the following conditional actions:

If  is odd, print Weird
If  is even and in the inclusive range of  to , print Not Weird
If  is even and in the inclusive range of  to , print Weird
If  is even and greater than , print Not Weird
Input Format

A single line containing a positive integer, .

Constraints

Output Format

Print Weird if the number is weird; otherwise, print Not Weird.
```
if __name__ == '__main__':
    n = int(raw_input())
    if n >= 1 and n<=100:
        # If n is odd, print Weird
        if n%2 != 0:
            print "Weird"
        else:
            if n>2 and n<5 or n>20:
                print "Not Weird"
            else:
                print "Weird"
      else:
        print "Weird"
```

### Task 2 (Arithmetic Operators)
Read two integers from STDIN and print three lines where:

The first line contains the sum of the two numbers.
The second line contains the difference of the two numbers (first - second).
The third line contains the product of the two numbers.
Input Format

The first line contains the first integer, a. The second line contains the second integer, b.

Constraints
 1 =< a =<100
 1 =< b =<100
 
 ```
 if __name__ == '__main__':
    a = int(raw_input())
    b = int(raw_input())
    import math
    if a >= 1 and a <= pow(10,10):
        if b >= 1 and b <= pow(10,10):
            print '%d' %(a+b)
            print '%d' %(a-b)
            print '%d' %(a*b)
 ```

### Task 3 (Division)
Read two integers and print two lines. The first line should contain integer division,  // . The second line should contain float division,  / .

You don't need to perform any rounding or formatting operations.

Input Format

The first line contains the first integer, . The second line contains the second integer, .

Output Format

Print the two lines as described above.

Sample Input 0
```
4
3
```
Sample Output 0
```
1
1.33333333333
```

```
from __future__ import division
if __name__ == '__main__':
    a = int(raw_input())
    b = int(raw_input())
    print "%d" %int(a/b)
    print "%f"  %(a/b)
```
 
### Task 4 (Loops)
Read an integer N. For all non-negative integers i < N, print (<i>i</i>)<sup>2</sup>. See the sample for details.

**Input Format**
The first and only line contains the integer, N.

**Constraints**
1 <= N <= 20

**Output Format**
Print N lines, one corresponding to each .

**Sample Input 0**
`5`

**Sample Output 0**
```
0
1
4
9
16
```

**Answer:**
```
if __name__ == '__main__':
    n = int(raw_input())
    i = 0
    for i in xrange (0, n):
        print pow(i,2)
```

### Task 5 (function)
We add a Leap Day on February 29, almost every four years. The leap day is an extra, or intercalary day and we add it to the shortest month of the year, February. 
In the Gregorian calendar three criteria must be taken into account to identify leap years:

The year can be evenly divided by 4, is a leap year, unless:
The year can be evenly divided by 100, it is NOT a leap year, unless:
The year is also evenly divisible by 400. Then it is a leap year.
This means that in the Gregorian calendar, the years 2000 and 2400 are leap years, while 1800, 1900, 2100, 2200, 2300 and 2500 are NOT leap years.Source

Task 
You are given the year, and you have to write a function to check if the year is leap or not.

Note that you have to complete the function and remaining code is given as template.

Input Format

Read y, the year that needs to be checked.

Constraints


Output Format

Output is taken care of by the template. Your function must return a boolean value (True/False)

Sample Input 0

1990
Sample Output 0

False

**Answer:**
```
def is_leap(year):
    leap = False
    
    if year >= 1900 and year <= pow(10, 5):
        if year % 4 == 0:
            leap = True
            
            if year % 100 == 0:
                leap = False
                
                if year % 400 == 0:
                    leap = True
    
    return leap
```
