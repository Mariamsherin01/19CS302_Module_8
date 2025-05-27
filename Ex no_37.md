# # Hackerrank problem - 2

Your task is to take two numbers of int data type, two numbers of float data type as input and output their sum:

Declare 4 variables: two of type int and two of type float.

Read 2 lines of input from stdin (according to the sequence given in the 'Input Format' section below) and initialize your variables.

Use the + and - operator to perform the following operations:

Print the sum and difference of two int variable on a new line.

Print the sum and difference of two float variable rounded to one decimal place on a new line.

## Input Format

The first line contains two integers.

The second line contains two floating point numbers.

## Constraints 

1 ≤ integer variables ≤ 104

1 ≤ float variables ≤ 104

## Output Format

Print the sum and difference of both integers separated by a space on the first line, and the sum and difference of both float (scaled to 1 decimal place) separated by a space on the second line.

Sample Input 

10 4

4.0 2.0

Sample Output 

14 6

6.0 2.0

Explanation

When we sum the integers 10 and 4, we get the integer 14. When we subtract the second number 4 from the first number 10, we get 6 as their difference.

When we sum the floating-point numbers 4.0 and 2.0, we get 6.0. When we subtract the second number 2.0 from the first number 4.0, we get 2.0 as their difference.


## Algorithm
1. Declare two int variables and two float variables.
2. Read two integers from input and assign them to the int variables.
3. Read two float numbers from input and assign them to the float variables.
4. Calculate and print the sum and difference of the two integers.
5. Calculate and print the sum and difference of the two floats rounded to one decimal place.

## Program
```
#include<stdio.h>
int main()
{
    int x,y;
    float a,b;
    scanf("%d %d",&x,&y);
    scanf("%f %f",&a,&b);
    printf("%d %d\n",x+y,x-y);
    printf("%.1f %.1f",a+b,a-b);
    
}
#include<stdio.h>
int main()
{
    int x,y;
    float a,b;
    scanf("%d %d",&x,&y);
    scanf("%f %f",&a,&b);
    printf("%d %d\n",x+y,x-y);
    printf("%.1f %.1f",a+b,a-b);
    
}
```

## Output

![image](https://github.com/user-attachments/assets/5583295b-3e42-40ba-8dfc-bbdc179f9191)

## Result

Thus the program was executed and the output was verified successfully.
