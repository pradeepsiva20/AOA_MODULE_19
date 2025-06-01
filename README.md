# EX 1A Factorial of a number
## DATE:
## AIM:
Write a Python Program to print factorial of a number recursively.

## Algorithm
1. Start the program and define a recursive function num_fact(n) to compute the factorial.
2. Inside the function, check if n is 0 or 1 — if so, return 1 (base case).
3. If not, return n * num_fact(n - 1) to continue recursion.
4. Read an integer input from the user. 
5. Call the function with the input value and print the result.  

## Program:
```python
/*
Program to implement Reverse a String
Developed by: PRADEEP S
Register Number: 212222100034 
*/
def num_fact(n):
    if n==0 or n==1:
        return 1

    return n*num_fact(n-1)
        
num=int(input())  
res = num_fact(num)
print(f"Factorial of number {num} = {res}")

```

## Output:

![image](https://github.com/user-attachments/assets/60aa690c-32b5-467c-af38-7b45bed03a30)



## Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
