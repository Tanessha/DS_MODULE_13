# EX 1 Display operator precedence in the infix expression.
## DATE: 06-03-2025
## AIM:
To write a C program to find and display the priority of the operator in the given Postfix expression

## Algorithm
1. Start the program.
2. Define the priority() function to return the priority of operators.
3. Initialize the string containing operators and operands.
4. Loop through each character in the string.
5. For each operator, call the priority() function to determine its priority.
6. Print the operator and its corresponding priority level.
7. End.
8. 
## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Tanessha Kannan
RegisterNumber: 212223040225

#include <stdio.h>
#include<string.h>

 int priorityg(char x)
{
    if(x == '&' || x == '|')
        return 1;
    else if(x=='+' || x=='-')
        return 2;
    else if(x=='*' || x=='/')
        return 4;
    else
        return -1;
}

int main()
{
   int i,j;
   char ch[100]= "100 200 + 2 / 5 * 7 |";
   for (i = 0; ch[i] != '\0'; i++) {
        if (ch[i] == '+' || ch[i] == '-' || ch[i] == '*' || ch[i] == '/' || ch[i] == '&' || ch[i] == '|') {
            j=priorityg(ch[i]);
            switch(j)
           {
               case 1:
               printf("%c  ----> Lowest Priority\n",ch[i]);
               break;
               case 2:
               printf("%c  ----> Second Lowest Priority\n",ch[i]);
               break;
               case 4:
               printf("%c  ----> Second Highest Priority\n",ch[i]);
               break;
               default:
               printf("Invalid\n");
           }
        }
   
    
    }return 0;
   
}
*/
```

## Output:
![image](https://github.com/user-attachments/assets/3a532fcf-1e32-4284-82c0-831c266d49c3)

## Result:
Thus the C program to find and display the priority of the operator in the given Postfix expression is implemented successfully
