Here are C language solutions for each problem from the PDF:

1. **Positive or Negative Number**
```c
#include <stdio.h>

int main() {
    float number;
    scanf("%f", &number);
    if (number >= 0)
        printf("Positive\n");
    else
        printf("Negative\n");
    return 0;
}
```

2. **Even or Odd Number**
```c
#include <stdio.h>

int main() {
    int number;
    scanf("%d", &number);
    if (number % 2 == 0)
        printf("Even\n");
    else
        printf("Odd\n");
    return 0;
}
```

3. **Digit in English**
```c
#include <stdio.h>

int main() {
    int digit;
    scanf("%d", &digit);
    char* digits_in_english[] = {"zero", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine"};
    printf("%s\n", digits_in_english[digit]);
    return 0;
}
```

4. **Valid Triangle**
```c
#include <stdio.h>

int main() {
    int angle1, angle2, angle3;
    scanf("%d %d %d", &angle1, &angle2, &angle3);
    if (angle1 + angle2 + angle3 == 180 && angle1 > 0 && angle2 > 0 && angle3 > 0)
        printf("Yes\n");
    else
        printf("No\n");
    return 0;
}
```

5. **Power of 2**
```c
#include <stdio.h>

int main() {
    int number;
    scanf("%d", &number);
    if (number > 0 && (number & (number - 1)) == 0)
        printf("Yes\n");
    else
        printf("No\n");
    return 0;
}
```

6. **Positive Nonzero Power of 2**
```c
#include <stdio.h>

int main() {
    int number;
    scanf("%d", &number);
    if (number > 0) {
        if ((number & (number - 1)) == 0)
            printf("Yes\n");
        else
            printf("No\n");
    } else if (number == 0) {
        printf("Zero is not a valid input\n");
    } else {
        printf("Negative input is not valid\n");
    }
    return 0;
}
```

7. **Comparison of Two Numbers**
```c
#include <stdio.h>

int main() {
    int x, y;
    scanf("%d %d", &x, &y);
    if (x > y)
        printf("%d is greater than %d\n", x, y);
    else if (x < y)
        printf("%d is less than %d\n", x, y);
    else
        printf("%d is equal to %d\n", x, y);
    return 0;
}
```

8. **Leap Year**
```c
#include <stdio.h>

int main() {
    int year;
    scanf("%d", &year);
    if ((year % 4 == 0 && year % 100 != 0) || year % 400 == 0)
        printf("Yes\n");
    else
        printf("No\n");
    return 0;
}
```

9. **Character Categorization**
```c
#include <stdio.h>

int main() {
    char ch;
    scanf(" %c", &ch);
    if ((ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z'))
        printf("Alphabet\n");
    else if (ch >= '0' && ch <= '9')
        printf("Digit\n");
    else
        printf("Special\n");
    return 0;
}
```

10. **Simple Expression Evaluation**
```c
#include <stdio.h>

int main() {
    float num1, num2;
    char operator;
    scanf("%f %c %f", &num1, &operator, &num2);
    if (operator == '+')
        printf("Addition: %.2f\n", num1 + num2);
    else if (operator == '-')
        printf("Subtraction: %.2f\n", num1 - num2);
    else if (operator == '*')
        printf("Multiplication: %.2f\n", num1 * num2);
    else if (operator == '/' && num2 != 0)
        printf("Division: %.2f\n", num1 / num2);
    else
        printf("Zero as divisor is not valid!\n");
    return 0;
}
```

11. **Grade Calculation**
```c
#include <stdio.h>

int main() {
    float score;
    scanf("%f", &score);
    if (score >= 90)
        printf("Grade: A\n");
    else if (score >= 86)
        printf("Grade: A-\n");
    else if (score >= 82)
        printf("Grade: B+\n");
    else if (score >= 78)
        printf("Grade: B\n");
    else if (score >= 74)
        printf("Grade: B-\n");
    else if (score >= 70)
        printf("Grade: C+\n");
    else if (score >= 66)
        printf("Grade: C\n");
    else if (score >= 62)
        printf("Grade: C-\n");
    else if (score >= 58)
        printf("Grade: D+\n");
    else if (score >= 55)
        printf("Grade: D\n");
    else
        printf("Grade: F\n");
    return 0;
}
```

12. **Arithmetic Operations Menu**
```c
#include <stdio.h>

int main() {
    float a, b;
    int choice;
    scanf("%f %f %d", &a, &b, &choice);
    if (choice == 1)
        printf("Addition: %.2f\n", a + b);
    else if (choice == 2)
        printf("Subtraction: %.2f\n", a - b);
    else if (choice == 3)
        printf("Multiplication: %.2f\n", a * b);
    else if (choice == 4 && b != 0)
        printf("Quotient: %.2f\n", a / b);
    else
        printf("Zero as divisor is not valid!\n");
    return 0;
}
```

13. **Advanced Arithmetic Operations Menu**
```c
#include <stdio.h>

int main() {
    float a, b;
    int choice, case_choice;
    scanf("%f %f %d", &a, &b, &choice);
    if (choice == 1)
        printf("Addition: %.2f\n", a + b);
    else if (choice == 2)
        printf("Subtraction: %.2f\n", a - b);
    else if (choice == 3)
        printf("Multiplication: %.2f\n", a * b);
    else if (choice == 4 && b != 0) {
        scanf("%d", &case_choice);
        if (case_choice == 1)
            printf("Quotient: %.2f\n", a / b);
        else
            printf("Remainder: %.2f\n", fmod(a, b));
    } else
        printf("Zero as divisor is not valid!\n");
    return 0;
}
```

14. **Division with Error Handling**
```c
#include <stdio.h>
#include <math.h>

int main() {
    float a, b;
    int choice, case_choice;
    scanf("%f %f %d", &a, &b, &choice);
    if (choice == 1)
        printf("Addition: %.2f\n", a + b);
    else if (choice == 2)
        printf("Subtraction: %.2f\n", a - b);
    else if (choice == 3)
        printf("Multiplication: %.2f\n", a * b);
    else if (choice == 4) {
        if (b != 0) {
            scanf("%d", &case_choice);
            if (case_choice == 1)
                printf("Quotient: %.2f\n", a / b);
            else
                printf("Remainder: %.2f\n", fmod(a, b));
        } else {
            printf("Error: Divisor is zero\n");
        }
    }
    return 0;
}
```

15. **Guessing Game**
```c
#include <stdio.h>

int main() {
    int x, n1, n2, n3;
    scanf("%d %d %d %d", &x, &n1, &n2, &n3);
    if (n1 == x)
        printf("Right, Player-2 wins!\n");
    else if (n2 == x) {
        printf("Wrong, 2 Chance(s) Left!\n");
        printf("Right, Player-2 wins!\n");
    } else if (n3 == x) {
        printf("Wrong, 2 Chance(s) Left!\n");
        printf("Wrong, 1 Chance(s) Left!\n");
        printf("Right, Player-2 wins!\n");
    } else {
        printf("Wrong, 2 Chance(s) Left!\n");
        printf("Wrong, 1 Chance(s) Left!\n");
        printf("Wrong, 0 Chance(s

) Left!\n");
        printf("Player-1 wins!\n");
    }
    return 0;
}
```
