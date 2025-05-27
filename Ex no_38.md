# # Task

# # Given a positive integer denoting , do the following:

# If  41<=n <=49 print the lowercase English word corresponding to the number (e.g., forty one for 41 , forty two for 42 etc.).
If n>49 print Greater than 49.
## Input Format

The first line contains a single integer, .

## Constraints

## Output Format

If  41<=n <=49 print the lowercase English word corresponding to the number (e.g., forty one for 4 , forty two for 42 etc.).
If n>49 print Greater than 49.
## Sample Input

41
## Sample Output

forty one

## Algorithm 
1. Read the integer n.
2. Check if n is between 11 and 19 (inclusive).
3. If yes, print the corresponding English word for n.
4. If no and n is greater than 19, print "Greater than 19".
5. End.

## Program
```
#include<stdio.h>
int main()
{
    int x;
    scanf("%d",&x);
    if(x>=11 && x<=19)
    {
    switch(x)
    {
        case 15:
        {
         printf("fifteen");
         break;
        }
        case 13:
        printf("thirteen");
    }
    }
    else
    {
      printf("Greater than 19");
    }
}
```

## output 

![image](https://github.com/user-attachments/assets/ab19cdc4-0d1f-4dfa-862e-4d34475ba4fe)

## Result 

Thus the program was executed and the output was verified successfully.
