# OS-Practical-Day_12-15.05.2025-

01. if- else condition structure:

if(condition){
  //body of if statment;
}
else{
  //body of else statment;
}

Q1. Enter your age and verify your aligible or not for election voting using if else condition 
 
#include <stdio.h>

int main() {
    int age;
    printf("Enter your age: ");
    scanf("%d", &age);
    if(age >= 18) {
        printf("You are eligible to vote.\n");
    } else {
        printf("You are not eligible to vote.\n");
    }
    return 0;
}

conclusion: The code correctly uses an if-else condition to check if the user's age is 18 or above to determine voting eligibility. It is syntactically and logically correct.

![age](https://github.com/user-attachments/assets/711de9f4-d0fd-466c-952b-7c1870c6e14b)

 
02. Rernary Operator structure:
test_condition ? expression1 : expression2;

03. Swith case structure
switch(variable/expression){
   case 1:
     //body of case 1
     break;
   case 2:
     //body of case 2
     break;

   case n:
     //body of case n
     break;

  default:
    // body of default
   }
   
Q2. Enter the value between 1 to 7 and create a program for following output:
Enter the number between 1 to 7 : 1
Today is Sunday!

#include <stdio.h>

int main() {
    int day;
    printf("Enter the number between 1 to 7: ");
    scanf("%d", &day);
    switch(day) {
        case 1:
            printf("Today is Sunday!\n");
            break;
        case 2:
            printf("Today is Monday!\n");
            break;
        case 3:
            printf("Today is Tuesday!\n");
            break;
        case 4:
            printf("Today is Wednesday!\n");
            break;
        case 5:
            printf("Today is Thursday!\n");
            break;
        case 6:
            printf("Today is Friday!\n");
            break;
        case 7:
            printf("Today is Saturday!\n");
            break;
        default:
            printf("Invalid input! Please enter a number from 1 to 7.\n");
    }
    return 0;
}

conclusion: The program takes a number between 1 and 7 as input and correctly uses a switch statement to display the corresponding weekday. It is logically and syntactically correct.

![days](https://github.com/user-attachments/assets/8787b8c7-67e7-4ab9-a41f-304997b0ca68)


Q3. write a code for small astrology based on your life path number for that  get date of birth 
from user then calculate life path number.(use switch case)
output:
   case 1-Date: 23
	 case 2-Date: 29
     calculation for life path number:                    
			  a=date%10     3                                
			  b=date/10     2
			  c=a+b         5
	  if life path number :
			  1:Lucky
			  2:Carefuly do your work
			  3:Storger
			  4:Happy
			  5:Can get help
			  6:Doubt
			  7:Sad 
			  8:Like
			  9:Courage
     
#include <stdio.h>

int main() {
    int date, a, b, lifePath;
    // Get the birth date from user
    printf("Enter your birth date (1 to 31): ");
    scanf("%d", &date);
    // Calculate life path number
    a = date % 10;
    b = date / 10;
    lifePath = a + b;
    // Reduce to single digit if needed
    if (lifePath > 9) {
        lifePath = (lifePath % 10) + (lifePath / 10);
    }
    // Display result using switch case
    printf("Your life path number is: %d\n", lifePath);
    printf("Astrology prediction: ");
    switch(lifePath) {
        case 1:
            printf("Lucky\n");
            break;
        case 2:
            printf("Carefully do your work\n");
            break;
        case 3:
            printf("Stronger\n");
            break;
        case 4:
            printf("Happy\n");
            break;
        case 5:
            printf("Can get help\n");
            break;
        case 6:
            printf("Doubt\n");
            break;
        case 7:
            printf("Sad\n");
            break;
        case 8:
            printf("Like\n");
            break;
        case 9:
            printf("Courage\n");
            break;
        default:
            printf("Invalid life path number\n");
    }
    return 0;
}

conclusion: The program correctly calculates the life path number from the entered birth date by summing its digits. It then uses a switch case to display a short astrology message based on that number. The logic is accurate and the code is syntactically correct.

![astrology](https://github.com/user-attachments/assets/3c28817e-3d0f-4455-a22f-7894b8529a1b)


Q4. Give list of numbers then calculate the summation and multiplication using for loop.
 Example:-
    1 2 3 4 5                             
	summation = 15                         
    multiplication =120

#include <stdio.h>

int main() {
    int n, i;
    int sum = 0, product = 1;
    printf("Enter how many numbers: ");
    scanf("%d", &n);
    int numbers[n];
    printf("Enter %d numbers: ", n);
    for(i = 0; i < n; i++) {
        scanf("%d", &numbers[i]);
    }
    for(i = 0; i < n; i++) {
        sum += numbers[i];
        product *= numbers[i];
    }
    printf("Summation = %d\n", sum);
    printf("Multiplication = %d\n", product);
    return 0;
}
conclusion: The program correctly reads a list of numbers from the user, then uses for loops to calculate and print their summation and multiplication. The code is logically and syntactically correct.

![summation](https://github.com/user-attachments/assets/451aa0d8-087e-4dc2-a97f-7c560853c1aa)

Q5. Print the integers from 1  to 10 using while loop.
#include <stdio.h>

int main() {
    int i = 1;
    while(i <= 10) {
        printf("%d ", i);
        i++;
    }
    printf("\n");
    return 0;
}
The program successfully prints integers from 1 to 10 using a while loop. It is correct and follows proper syntax and logic.

![while loop](https://github.com/user-attachments/assets/33758677-d5b5-4cb7-832c-7337701d67b7)


Q6. Write a C program to generate and print the Fibonacci series up to a specified 
number of terms. The program should take the number of terms as input from the 
user and then display the corresponding Fibonacci sequence.

#include <stdio.h>

int main() {
    int n, i;
    int t1 = 0, t2 = 1, nextTerm;
    printf("Enter the number of terms: ");
    scanf("%d", &n);
    printf("Fibonacci Series: ");
    for(i = 1; i <= n; i++) {
        printf("%d ", t1);
        nextTerm = t1 + t2;
        t1 = t2;
        t2 = nextTerm;
    }
    printf("\n");
    return 0;
}

conclusion: The program correctly generates and prints the Fibonacci series up to the specified number of terms input by the user. It uses a for loop and updates terms in each iteration.

![Fibonacci](https://github.com/user-attachments/assets/14a51e91-9ff3-4dfc-9253-7d0847c7437f)


Q7. Write a C program to calculate the factorial of a given non-negative integer.  
 #include <stdio.h>

int main() {
    int n, i;
    unsigned long long factorial = 1;
    printf("Enter a non-negative integer: ");
    scanf("%d", &n);
    if(n < 0) {
        printf("Factorial is not defined for negative numbers.\n");
    } else {
        for(i = 1; i <= n; i++) {
            factorial *= i;
        }
        printf("Factorial of %d is %llu\n", n, factorial);
    }
    return 0;
}

conclusion: The program correctly calculates the factorial of a non-negative integer using a for loop. It handles negative inputs by displaying an appropriate message. The code is syntactically and logically correct.

![Factorial](https://github.com/user-attachments/assets/e85b9178-01b1-4bbb-8676-ee3896a128bc)


Q8. 
Write a C program that:
Accepts two strings as input from the user.
Concatenates the two strings Displays the concatenated result.

#include <stdio.h>
#include <string.h>

int main() {
    char str1[100], str2[100];
    // Get input strings from user
    printf("Enter first string: ");
    fgets(str1, sizeof(str1), stdin);
    printf("Enter second string: ");
    fgets(str2, sizeof(str2), stdin);
    // Remove newline characters if present
    str1[strcspn(str1, "\n")] = '\0';
    str2[strcspn(str2, "\n")] = '\0';
    // Concatenate strings
    strcat(str1, str2);
    // Display result
    printf("Concatenated string: %s\n", str1);
    return 0;
}

Conclusion: The program accepts two strings, removes trailing newline characters, concatenates them using strcat, and displays the combined string. It handles input safely and works correctly.

![Concat](https://github.com/user-attachments/assets/d61c23de-6806-43fd-8b8d-09f9654b7f2b)

     
