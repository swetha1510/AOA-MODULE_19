# EX 1A Reverse a String
## DATE:
## AIM:
To write a program to create a recursive function to reverse a string.

## Algorithm
1. Input the string s.
2. Define a recursive function reverse(s)
i) If len(s) == 1, return s.
ii) Otherwise, return s[-1] + reverse(s[:-1]).
3. Call reverse(s) to reverse the string.
4.  The function recursively reverses the string by appending characters from the end.
5. Print the reversed string.
## Program:
```
/*
Program to implement Reverse a String
Developed by: SWETHA P
Register Number: 212222100053
*/

def reverse(s):
    if len(s)==1:
        return s[0]
    else:
        
        return s[-1]+reverse(s[:-1])
s=input()
print(reverse(s))
```

## Output:
![438660955-c191ad44-8f10-4593-aa31-cd2996a9ed3d](https://github.com/user-attachments/assets/54818f55-d4f5-4a09-b1cd-aa03caadd38f)

## Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
