## EXP NO 2A : C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER

## Aim:
To write a C program print the lowercase English word corresponding to the number

## Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
## Program:
~~~
#include<stdio.h>
int main ()
{
    int n;
    scanf("%d",&n);
    if(n>=71)
    {
        if(n<=79)
        {
           int g=n%10;
           switch(g)
             {
              case 1:
                printf("seventy one");
                 break;
case 2:
                printf("seventy two");
                 break;
case 3:
                printf("seventy three");
                 break;
case 4:
                printf("seventy four");
                 break;
case 5:
                printf("seventy five");
                 break;
case 6:
                printf("seventy six");
                 break;
case 7:
                printf("Seventy seven");
                 break;
case 8:
                printf("seventy eight");
                 break;
default:
                printf("seventy nine");
                 
             }

        }
else
{
printf("Greater than 79");
}
        
    }
else
{
printf("Less than 71");
}
return 0;
}
~~~
## Output:
![Screenshot 2025-06-01 230823](https://github.com/user-attachments/assets/36de179c-71bc-4458-b5ee-fd00995c04f4)


## Result:
Thus, the program is verified successfully


 
## EXP NO 2B : C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .

## Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.

## Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
## Program:
#include<stdio.h>
#include<string.h>
int main ()
{
    char c[20];
    scanf("%s",c);
    int m=strlen(c);
    for(int i=0;i<=9;i++)
    {
        int h=0;
        
        for(int j=0;j<m;j++)
        {
            int q=c[j]-'0';
            if(i==q)
            {
                h++;
            }
        }
        printf("%d ",h);
    }
    return 0;
}
~~~




## Output:
![Screenshot 2025-06-01 231148](https://github.com/user-attachments/assets/90132b69-1bc7-4439-91f9-a2907159cc66)


## Result:
Thus, the program is verified successfully



## EXP NO 2C : C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.

## Aim:
To write a C program to print all of its permutations in strict lexicographical order.

## Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)
3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
## Program:
~~~
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <stdbool.h>

int compare_strings(const void *a, const void *b) {
    return strcmp(*(const char **)a, *(const char **)b);
}

bool next_permutation(char **arr, int n) {
    int i = n - 2;
    while (i >= 0 && strcmp(arr[i], arr[i + 1]) >= 0) {
        i--;
    }
    if (i < 0) {
        return false;
    }
    int j = n - 1;
    while (strcmp(arr[i], arr[j]) >= 0) {
        j--;
    }
    char *temp = arr[i];
    arr[i] = arr[j];
    arr[j] = temp;
    qsort(arr + i + 1, n - i - 1, sizeof(char *), compare_strings);
    return true;
}

int main() {
    int n;
    scanf("%d", &n);
    char **arr = (char **)malloc(n * sizeof(char *));
    for (int i = 0; i < n; i++) {
        arr[i] = (char *)malloc(101 * sizeof(char));
        scanf("%s", arr[i]);
    }
    qsort(arr, n, sizeof(char *), compare_strings);

    do {
        for (int i = 0; i < n; i++) {
            printf("%s%c", arr[i], (i == n - 1) ? '\n' : ' ');
        }
    } while (next_permutation(arr, n));

    for (int i = 0; i < n; i++) {
        free(arr[i]);
    }
    free(arr);
    return 0;
}
~~~
## Output:
![Screenshot 2025-06-01 231244](https://github.com/user-attachments/assets/eeefc2a1-1f52-4950-93a0-b9fa7989c922)

## Result:
Thus, the program is verified successfully


 
## EXP NO 2D : C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.

## Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.

## Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
## Program:
~~~
#include<stdio.h>
int main ()
{
    int n;
    scanf("%d",&n);
    for(int p=n;p>1;p--)
    {
        for(int i=n;i>1;i--)
        {
            if(p>i)
            {
                printf("%d ",p);
            }
            else
            {
                printf("%d ",i);
            }
        }
        for(int j=1;j<=n;j++)
        {
             if(p>j)
            {
                printf("%d ",p);
            }
            else
            {
                printf("%d ",j);
            }
        }
    
        
        printf("\n");
    }
    for(int p=1;p<=n;p++)
    {
        for(int i=n;i>1;i--)
        {
            if(p>i)
            {
                printf("%d ",p);
            }
            else
            {
                printf("%d ",i);
            }
        }
        for(int j=1;j<=n;j++)
        {
             if(p>j)
            {
                printf("%d ",p);
            }
            else
            {
                printf("%d ",j);
            }
        }
    
        
        printf("\n");
    }
    
    return 0;
}
~~~

## Output:
![Screenshot 2025-06-01 231400](https://github.com/user-attachments/assets/1b930121-8b74-4f98-9cd9-b14d55b97922)

## Result:
Thus, the program is verified successfully



## EXP NO 2E : C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

## Aim:
To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

## Algorithm:
1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

## Program:
~~~
#include <stdio.h>
void square();
int main(){  
    square();
    return 0;
}
void square(){
    int a;
    scanf("%d",&a);
    float ans = a*a;
    printf("The square of %d is : %.2f",a,ans);
}
~~~
## Output:
![437943571-6adbadf8-a2c4-40bc-9972-503f6b5fc550](https://github.com/user-attachments/assets/ee623add-e7c8-42f6-abd8-cd4061604ab6)

## Result:
Thus, the program is verified successfully
