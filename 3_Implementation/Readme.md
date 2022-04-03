#include <stdio.h>  
#include <conio.h>  
#include <math.h>  
#include <stdlib.h>    
int add();  
int subtract();  
int multiply();  
int divide();  
int sq();  
int sqroot();  
void exit();  
int main()  
{  
    int choi;  
    do  
    {  
        printf (" Select any of the given options to perform calculation: ");  
        printf (" \n 1 Add \t \t 2 Subtract \n 3 Multiply\t 4 Divide\n 5 Square \t \t 6 Square Root \n 7 Exit \n \n Give any of one choice ");      
        scanf ("%d", &choi);
    switch (choi)  
    {  
        case 1:  
            add();
            break;
        case 2:  
            subtract();  
            break;  
        case 3:  
            multiply();
            break;  
        case 4:  
            divide();  
            break;
        case 5:  
            sq();  
            break;
        case 6:  
            sqroot();
            break;
        case 7:  
            exit(0);
            break;  
        default:  
            printf(" Wrong option ");  
            break;                        
    }  
    printf (" \n \n ********************************************** \n ");  
    } while (choi != 7);  
    return 0;        
}  
int add()  
{  
    int i, sum = 0, num, f_num;
    printf (" How many numbers: ");  
    scanf ("%d", &num);  
    printf (" Enter the numbers: \n ");  
    for (i = 1; i <= num; i++)  
    {  
        scanf(" %d", &f_num);  
        sum = sum + f_num;  
    }  
    printf (" Sum of the numbers = %d", sum);  
    return 0;  
}  
int subtract()  
{  
    int i, sub = 0, num, f_num;
    printf (" How many numbers: ");  
    scanf ("%d", &num);  
    printf (" Enter the numbers: \n ");  
    for (i = 1; i <= num; i++)  
    {  
        scanf(" %d", &f_num);  
        if(i==1)sub=f_num;
       if(i!=1)
       {
           sub=sub-f_num;
       }
    }  
    printf (" Substract of the numbers = %d", sub);  
    return 0;  
}  
 
int multiply()  
{  
    int i, mul = 1, num, f_num;
    printf (" How many numbers: ");  
    scanf ("%d", &num);  
    printf (" Enter the numbers: \n ");  
    for (i = 1; i <= num; i++)  
    {  
        scanf(" %d", &f_num);  
       mul=mul*f_num;
       
    }  
    printf (" Multiply of the numbers = %d", mul);  
    return 0;    
}  

int divide()  
{  
    int n1, n2, res;  
    printf (" Enter the first number : ");  
    scanf (" %d", &n1);  
    printf (" Enter the second number : ");  
    scanf (" %d", &n2);  
     
    if (n2 == 0)  
    {  
        printf (" \n Divisor cannot be zero. Enter another value ");  
        scanf ("%d", &n2);        
    }  
    res = n1 / n2;    
    printf (" \n The divide of %d / %d is: %d", n1, n2, res);  
}  
 
int sq()  
{  
    int n1, res;  
    printf (" Enter a number : ");  
    scanf (" %d", &n1);  
     
    res = n1 * n1;    
    printf (" \n The Square of %d is: %d", n1, res);  
}  
 
int sqroot()  
{  
    float res;  
    int n1;  
    printf (" Enter a number: ");  
    scanf (" %d", &n1);  
 
    res = sqrt(n1);  
    printf (" \n The Square Root of %d is: %f", n1, res);  
}


