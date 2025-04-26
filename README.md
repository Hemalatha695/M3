# EX-11-EMI-CALCULATOR

## AIM

To write a program to prepare EMI calculator using function without return type and with arguments.

## ALGORITHM

1.	Start the program.
2.	Read principal amount, rate of interest and months.
3.	Pass these values as arguments to function.
4.	Calculate EMI using the formula, amt=(prpow(1+r,t))/(pow(1+r,t)-1)
5.	Display the result.
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <math.h>

// Step 3: Function prototype
void calculateEMI(float principal, float rate, int months);

int main() {
    // Step 2: Read inputs
    float principal, rate;
    int months;

    printf("Enter principal amount: ");
    scanf("%f", &principal);

    printf("Enter annual interest rate (in percentage): ");
    scanf("%f", &rate);

    printf("Enter number of months (loan tenure): ");
    scanf("%d", &months);

    // Step 3: Call function
    calculateEMI(principal, rate, months);

    return 0;
}

// Step 4: Function definition
void calculateEMI(float principal, float rate, int months) {
    float monthlyRate, emi;

    // Convert annual rate to monthly and percentage to decimal
    monthlyRate = rate / (12 * 100);

    // EMI formula
    emi = (principal * monthlyRate * pow(1 + monthlyRate, months)) /
          (pow(1 + monthlyRate, months) - 1);

    // Step 5: Display result
    printf("Monthly EMI = ₹%.2f\n", emi);
}
```

## OUTPUT
```
Enter principal amount: 50000
Enter annual interest rate (in percentage): 12
Enter number of months (loan tenure): 12
Monthly EMI = ₹4449.45
```




## RESULT

Thus the program to prepare EMI calculator using function without return type with arguments has been executed successfully
 
 


# EX-12-FIBONACCI-SERIES
## AIM
To write a C program to generate the Fibonacci series for the value 6.

## ALGORITHM
1.	Start the program.
2.	Read number of terms to display.
3.	Add the previous two terms and store it in new term.
4.	Assign 2nd term to 1st term and 3rd term to 2nd term.
5.	Repeat steps 3 and 4 n number of times.
6.	Display the result.
7.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    // Step 1 & 2: Initialization and input
    int n = 6; // Fixed value as per the question
    int first = 0, second = 1, next;

    printf("Fibonacci series for %d terms:\n", n);

    // Print the first two terms
    printf("%d %d ", first, second);

    // Step 3–5: Generate remaining terms
    for (int i = 3; i <= n; i++) {
        next = first + second;    // Step 3: Add previous two terms
        printf("%d ", next);      // Step 6: Display result
        first = second;           // Step 4: Move terms forward
        second = next;
    }

    printf("\n"); // New line for clean output
    return 0;     // Step 7: End the program
}
```
## OUTPUT
```
Fibonacci series for 6 terms:
0 1 1 2 3 5
```







## RESULT
Thus the program to generate the Fibonacci series for the value 6 has been executed successfully.
 
 


# EX-13-ONE-DIMENSIONAL-ARRAY
## AIM
To write a C program to read n elements as input and print the last element of the array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	Print the last element.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    // Step 2: Declare variable
    int n;

    // Step 2: Read number of elements
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    // Step 3: Declare array and read values
    int arr[n];
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Step 4: Print the last element
    printf("Last element of the array: %d\n", arr[n - 1]);

    return 0; // Step 5: Stop the program
}
```
## OUTPUT
```
Enter the number of elements: 5
Enter 5 elements:
10 20 30 40 50
Last element of the array: 50
```


## RESULT
Thus the program to read n elements as input and print the last element of the array has been executed successfully.
 
 


# EX-14-POSITIVE-ARRAY-ELEMENTS
## AIM
To write a C Program to count total number of positive elements in an array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	If the array value can be divided by 2 then increment count by 1.
5.	Display result.
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    // Step 2: Read number of elements
    int n;
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    // Step 3: Read array elements
    int arr[n], count = 0;
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);

        // Step 4: Check if element is positive
        if (arr[i] > 0) {
            count++;
        }
    }

    // Step 5: Display result
    printf("Total number of positive elements: %d\n", count);

    return 0; // Step 6: Stop the program
}
```

## OUTPUT
```
Enter the number of elements: 6
Enter 6 elements:
-3 5 0 8 -1 4
Total number of positive elements: 3
```




## RESULT
Thus the program to count total number of positive elements in an array has been executed successfully.





 
 


# EX -15 - Replace All Even Elements With 'E' In One Dimensional Array

## Aim:
To write a C program to replace all even elements with 'E' in one dimensional array

## Algorithm:
1.	Input the array:
  Read the size of the array.
  Input the elements of the array.
2.	Iterate through the array:
 	For each element of the array, check if the element is even (i.e., if the element modulo 2 equals 0).
3.	Replace even elements with 'E':
     If an element is even, replace that element with the character 'E'.
4.	Output the updated array:
 Print the updated array after replacements.

## Program:
```
#include <stdio.h>

int main() {
    int n;

    // Step 1: Read size and elements
    printf("Enter the size of the array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d integer elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Step 2 & 3: Replace even elements with 'E'
    printf("Updated array:\n");
    for (int i = 0; i < n; i++) {
        if (arr[i] % 2 == 0) {
            printf("E ");
        } else {
            printf("%d ", arr[i]);
        }
    }

    printf("\n");
    return 0;
}
```
## Output:
```
Enter the size of the array: 6
Enter 6 integer elements:
3 8 5 2 9 4
Updated array:
3 E 5 E 9 E
```


## Result:

Thus, the program to replace all even elements with 'E' in one dimensional array was verified successfully.



