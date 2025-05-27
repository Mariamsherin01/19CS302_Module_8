## Given an array of strings sorted in lexicographical order, print all of its permutations in strict lexicographical order. If two permutations look the same, only print one of them. See the 'note' below for an example.

Complete the function next_permutation which generates the permutations in the described order.

## For example, s=[ab,bc,cd]. The six permutations in correct order are:

ab bc cd
ab cd bc
bc ab cd
bc cd ab
cd ab bc
cd bc ab
Note: There may be two or more of the same string as elements of .
## For example, s=[ab,bc,cd]. Only one instance of a permutation where all elements match should be printed. In other words, if s[0]==s[1], then print either s[0]  or s[1] but not both.

A three element array having three distinct elements has six permutations as shown above. In this case, there are three matching pairs of permutations where ab and ba are switched. We only print the three visibly unique permutations:

ab ab bc
ab bc ab
bc ab ab
## Input Format

The first line of each test file contains a single integer , the length of the string array .

Each of the next  lines contains a string .

Constraints

 contains only lowercase English letters.
Output Format

Print each permutation as a list of space-separated strings on a single line.

## Sample Input 0

2
ab
cd
## Sample Output 0

ab cd
cd ab
## Sample Input 1

3
a
bc
bc
## Sample Output 1

a bc bc
bc a bc
bc bc a

## Algorithm
1. Start with the array sorted in lexicographical order.
2. Print the current permutation.
3. Generate the next permutation using the following steps:
   a. Find the largest index i such that array[i] < array[i + 1]. If no such i exists, all permutations are generated.
   b. Find the largest index j greater than i such that array[i] < array[j].
   c. Swap array[i] and array[j].
   d. Reverse the sub-array from i+1 to the end.
4. Skip duplicate permutations by checking if the current permutation matches the previous one before printing.
5. Repeat steps 2-4 until all unique permutations are printed.

## Program 
```
#include<stdio.h>
#include<stdlib.h>
#include<string.h>

void swap(char **s,int i,int j)
{
    char *temp = s[i];
    s[i] = s[j];
    s[j] = temp;
}
void rev(char **s,int start,int end)
{
    while(start<end)
    {
        swap(s,start++,end--);
    }
}
int per(int n,char **s)
{
    int i,j;
    for(i=n-2;i>-1;i--)
    {
        if(strcmp(s[i+1],s[i])>0)
        {
            for(j=n-1;j>i;j--)
            {
                if(strcmp(s[j],s[i])>0)
                {
                    swap(s,i,j);
                    rev(s,i+1,n-1);
                    return 1;
                }
                
            }
            
        }
    }
    return 0;
}

int main()
{
    int n,i;
    scanf("%d",&n);
    char **s;
    s = calloc(n,sizeof(char*));
    for(i=0;i<n;i++)
    {
        s[i]=calloc(11,sizeof(char));
        scanf("%s",s[i]);
    }
    do
    {
        for(i=0;i<n;i++)
        {
            printf("%s%c",s[i],i==n-1?'\n':' ');
        }
        
    }
    while(per(n,s));
    {
        for(i=0;i<n;i++)
        free(s[i]);
        free(s);
        return 0;
}
}
```
## Output

![image](https://github.com/user-attachments/assets/1e0278e2-a42b-4b82-a003-5cbd40d561ee)

## Result 
Thus the program was executed and the output was verified successfully.
