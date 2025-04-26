EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
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
 
Program:
```
#include<stdio.h>
int main()
{
    int n;
    scanf("%d",&n);
    switch (n)
    {
        case 11:
            printf("eleven");
            break;
        case 12: 
            printf("twelve");
            break;
        case 13:
            printf("thirteen");
            break;
        case 14:
            printf("fourteen");
            break;
        case 15:
            printf("fifteen");
            break;
        default:
            printf("Greater than 19");
        }
    
}

```
Output:

![image](https://github.com/user-attachments/assets/a8812a6e-6917-496a-85a5-5ba6b18dfda5)


Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:
```
#include<stdio.h>
#include<ctype.h>
#include<string.h>
int main()
{
    char s[100];
    int f[10]={0};
    scanf("%s",s);
    for(int i=0;s[i]!='\0';i++){
    if(isdigit(s[i]))
    {
        int d= s[i]- '0';
        f[d]++;
    }
    }
    for(int i=0;i<10;i++){
    printf("%d ",f[i]);
    }
}
```
Output:

![image](https://github.com/user-attachments/assets/fae1bde4-aba3-49eb-a9cf-3db21ba577a5)


Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
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
 
Program:
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
int next_permutation(int n, char **s)
{
    int k = -1;
    for (int i = 0; i < n-1; i++) {
        if (strcmp(s[i], s[i+1]) < 0)
            k = i;
    }
    if (k == -1) 
        return 0; 
    int l = -1;
    for (int i = k+1; i < n; i++) {
        if (strcmp(s[k], s[i]) < 0)
            l = i;
    }
    char *tmp = s[k];
    s[k] = s[l];
    s[l] = tmp;
    int i = k+1, j = n-1;
    while (i < j) {
        tmp = s[i];
        s[i++] = s[j];
        s[j--] = tmp;
    }
    return 1; 
}
int main()
{
	char **s;
	int n;
	scanf("%d", &n);
	s = calloc(n, sizeof(char*));
	for (int i = 0; i < n; i++)
	{
		s[i] = calloc(n, sizeof(char));
		scanf("%s", s[i]);
	}
	do
	{
		for (int i = 0; i < n; i++)
			printf("%s%c", s[i], i == n - 1 ? '\n' : ' ');
	} while (next_permutation(n, s));
	for (int i = 0; i < n; i++)
		free(s[i]);
	free(s);
	return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/1a331513-d6e2-43a9-8517-0f2434bbff79)


Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:
```
#include<stdio.h>
int main()
{
int n,i,j,min;
scanf("%d",&n);
int len=n*2-1; 
for (i=0;i<len;i++)
{
for (j=0;j<len;j++)
{
min=i<j?i:j;
min=min<len-i-1?min:len-1-i;
min=min<len-j-1?min:len-1-j;
printf("%d ",n-min);
}
printf("\n");
}
return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/3ac13cf6-9cba-40ad-83af-4910992fce41)


Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

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

Program:
```
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
```
Output:

![image](https://github.com/user-attachments/assets/7e4f34f2-51b3-4da9-a22d-5daf0dfeffd9)


Result:
Thus, the program is verified successfully



























