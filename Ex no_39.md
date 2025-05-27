# EX 39 C program to find sum of digits.
## AIM:
To write a C program to find sum of digits.

## Algorithm
1. Read the five-digit integer n.
2. Initialize sum to 0.
3. Repeat while n > 0:
   - Extract the last digit using digit = n % 10.
   - Add digit to sum.
   - Remove the last digit using n = n / 10.
4. After loop ends, print the sum.
5. End.


## Program:
```
/*
C program to find sum of digits.
Developed by:  Mariam Sherin
RegisterNumber: 212222060143
 #include<stdio.h>
int main()
{
    int n,sum=0;
    scanf("%d",&n);
    while(n!=0){
        int last=n%10;
        sum=sum+last;
        n=n/10;
    }printf("%d",sum);
}

*/
```

## Output:

![image](https://github.com/user-attachments/assets/2d1e784e-8d50-459f-9a06-a53734c64bb4)


## Result:
Thus the program was executed and the output was verified successfully.
