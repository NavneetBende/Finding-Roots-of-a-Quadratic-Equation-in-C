# Finding-Roots-of-a-Quadratic-Equation-in-C

Finding Roots of a Quadratic Equation in C
In this C program, we will find the roots of a quadratic equation [ax2 + bx + c]. We can solve a Quadratic Equation by finding its roots. Mainly roots of the quadratic equation are represented by a parabola in 3 different patterns like :

No Real Roots
One Real Root
Two Real Roots
Roots of a quadratic equation in C
While loop in C
Algorithm :
Calculate Discriminant (D)
D = b^2 – 4*a*c
If D>0 : Two real root exists.
If D=0 : Equal root exists.
If D<0 : Imaginary root exists.
Related Pages
Finding Number of times x digit occurs in a given input
 
Finding number of integers which has exactly x divisors
 
Power of a Number 

Prime Number

Largest element in an array

Code in C
Run
/* Write a program to find roots of a quadratic equation in C */
#include <stdlib.h>
#include <stdio.h>
#include <math.h>
 
void findRoots(int a, int b, int c)
{
    if (a == 0) {
        printf("Invalid");
        return;
    }
 
    int d = b * b - 4 * a * c;
    double sqrt_val = sqrt(abs(d));
 
    if (d > 0) {
        printf("Roots are real and different \n");
        printf("%f\n%f", (double)(-b + sqrt_val) / (2 * a),(double)(-b - sqrt_val) / (2 * a));
    }
    else if (d == 0) {
        printf("Roots are real and same \n");
        printf("%f", -(double)b / (2 * a));
    }
    else // d < 0
    {
        printf("Roots are complex \n");
        printf("%f + i%f\n%f - i%f", -(double)b / (2 * a), sqrt_val/(2 * a), -(double)b / (2 * a), sqrt_val/(2 * a));
    }
}
 
int main()
{
    int a = 1, b = 4, c = 4;
   
    findRoots(a, b, c);
    return 0;
}
Output :
Roots are real and same 
-2.000000
