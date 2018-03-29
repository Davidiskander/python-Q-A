### Task 1 (If-else Statement)
Given an integer, N, perform the following conditional actions:

- If N is odd, print Weird
- If N is even and in the inclusive range of 2 to 5, print Not Weird
- If N is even and in the inclusive range of 6 to 20, print Weird
- If N is even and greater than 20, print Not Weird

**Input Format:** A single line containing a positive integer, N.
**Constraints:** 1 <= n <=100
**Output Format:** Print Weird if the number is weird; otherwise, print Not Weird.

**Answer:**
```
if __name__ == '__main__':
    n = int(raw_input())
    if n >= 1 and n<=100:
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
Read two integers and print two lines. The first line should contain integer division, a/b . The second line should contain float division, a/b. You don't need to perform any rounding or formatting operations.

**Input Format:** The first line contains the first integer. The second line contains the second integer, .
**Output Format:** Print the two lines as described above.

**Sample Input:**
4
3

**Sample Output:**
1
1.33333333333

**Answer:**
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

**Input Format:** The first and only line contains the integer, N.
**Constraints:** 1 <= N <= 20
**Output Format:** Print N lines, one corresponding to each .

**Sample Input:** `5`
**Sample Output:**
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
write a function that takes a variable "year" and returns True/False if it is leap year or not.

**How to know if it's a leap year:**
- The year can be evenly divided by 4, is a leap year, unless:
- The year can be evenly divided by 100, it is NOT a leap year, unless:
- The year is also evenly divisible by 400. Then it is a leap year.

**Input Format:** 4 digits year
**Constraints:** year >= 1900 and year <= pow(10, 5):
**Output Format:** Your function must return a boolean value (True/False)

**Sample Input:** 1990
**Sample Output:** False

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

### Task 6
Read an integer N. Without using any string methods, try to print the following:

**Input Format** an integer "n".
**Output Format** ex:12345......n

**Sample Input:** 3
**Sample Output:** 123

**Answer:**
```
if __name__ == '__main__':
    n = int(raw_input())
    i = 2
    str = '1'
    for i in xrange (i, n+1):
        str += `i`
    print (str) 
```

### Task 7 (swap case)
You are given a string and your task is to swap cases. In other words, convert all lowercase letters to uppercase letters and vice versa.

For Example:
DaVId → dAviD
Pythonist 2 → pYTHONIST 2

```
def swap_case(s):
    if len(s) > 0 and len(s) <= 1000: 
        x = s.swapcase()
        return x
```

### Task 8 (count and print unique words in a string)
```
def count_print_unique_words(str):
    words_list = str.split()
    words_list = [x.lower() for x in words_list]
    unique_list = list(set(words_list))
    sorted_list = sorted(unique_list)
    for i in sorted_list:
        print "%s - %s" % (i, words_list.count(i))
```

### Task 9 (You are given an immutable string, and you want to make changes to it)
```
def mutate_string(string, position, character):
    l = list(string)
    l[position] = character
    string = ''.join(l)
    return string
```

