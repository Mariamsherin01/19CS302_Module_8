# # #Task - Hackerrank Problem

This challenge requires you to print Hello Saveetha! on a single line, and then print the already provided input string to stdout. If you are not familiar with C, you may want to read about the printf() command.

# # Example:

Saveetha

The required output is: Hello, Saveetha! C Programming

## Algorithm

1. Print "Good Morning!" on a new line.
2. Read the input string from the user.
3. Print the input string on the next line.
4. End.

## Program 
```
#include<stdio.h>
int main()
{
    char s[30];
    scanf("%[^\n]",s);
    printf("Good Morning!\n%s",s);
}
```

## Output

![image](https://github.com/user-attachments/assets/d82bb545-3a9f-4f29-b6a4-accf19e2fed9)

## Result 





