Here are the C language solutions for the loop-related problems from the PDF:

1. **Print Series up to N Terms**
```c
#include <stdio.h>

int main() {
    int N;
    scanf("%d", &N);
    for (int i = 1; i <= N; i++) {
        printf("%d", i);
        if (i < N)
            printf(", ");
    }
    printf("\n");
    return 0;
}
```

2. **Print Odd Series up to N Terms**
```c
#include <stdio.h>

int main() {
    int N;
    scanf("%d", &N);
    for (int i = 1; i <= 2 * N - 1; i += 2) {
        printf("%d", i);
        if (i < 2 * N - 1)
            printf(", ");
    }
    printf("\n");
    return 0;
}
```

3. **Print Alternating 1, 0 Series**
```c
#include <stdio.h>

int main() {
    int N;
    scanf("%d", &N);
    for (int i = 1; i <= N; i++) {
        printf("%d", i % 2);
        if (i < N)
            printf(", ");
    }
    printf("\n");
    return 0;
}
```

4. **Compute Average of N Numbers**
```c
#include <stdio.h>

int main() {
    int N;
    float number, sum = 0;
    scanf("%d", &N);
    for (int i = 0; i < N; i++) {
        scanf("%f", &number);
        sum += number;
    }
    printf("AVG of %d inputs: %.6f\n", N, sum / N);
    return 0;
}
```

5. **Square X and Increment/Decrement until X Reaches Y**
```c
#include <stdio.h>

int main() {
    int X, Y;
    scanf("%d %d", &X, &Y);
    while (X != Y) {
        printf("%d, ", X * X);
        if (X < Y)
            X++;
        else
            X--;
    }
    printf("Reached!\n");
    return 0;
}
```

6. **Guessing Game**
```c
#include <stdio.h>

int main() {
    int X, N, guess;
    scanf("%d %d", &X, &N);
    for (int i = 1; i <= N; i++) {
        scanf("%d", &guess);
        if (guess == X) {
            printf("Right, Player-2 wins!\n");
            return 0;
        } else {
            printf("Wrong, %d Choice(s) Left!\n", N - i);
        }
    }
    printf("Player-1 wins!\n");
    return 0;
}
```

7. **Show Inputs Until User Types 'A'**
```c
#include <stdio.h>

int main() {
    char input;
    int count = 1;
    while (1) {
        scanf(" %c", &input);
        if (input == 'A')
            break;
        printf("Input %d: %c\n", count, input);
        count++;
    }
    return 0;
}
```

8. **Reverse Digits of an Integer**
```c
#include <stdio.h>

int main() {
    int number, reversed = 0;
    scanf("%d", &number);
    while (number != 0) {
        reversed = reversed * 10 + number % 10;
        number /= 10;
    }
    printf("%d\n", reversed);
    return 0;
}
```

9. **Find Grade for N Students**
```c
#include <stdio.h>

int main() {
    int N;
    float A, HW, CT, MT, TF, total;
    scanf("%d", &N);
    for (int i = 1; i <= N; i++) {
        scanf("%f %f %f %f %f", &A, &HW, &CT, &MT, &TF);
        total = (A * 0.05) + (HW * 0.10) + (CT * 0.15) + (MT * 0.30) + (TF * 0.40);
        printf("Student %d : ", i);
        if (total >= 90)
            printf("A\n");
        else if (total >= 86)
            printf("A-\n");
        else if (total >= 82)
            printf("B+\n");
        else if (total >= 78)
            printf("B\n");
        else if (total >= 74)
            printf("B-\n");
        else if (total >= 70)
            printf("C+\n");
        else if (total >= 66)
            printf("C\n");
        else if (total >= 62)
            printf("C-\n");
        else if (total >= 58)
            printf("D+\n");
        else if (total >= 55)
            printf("D\n");
        else
            printf("F\n");
    }
    return 0;
}
```

10. **Sum of Series 1, -2, 3, -4, ...**
```c
#include <stdio.h>

int main() {
    int N, sum = 0;
    scanf("%d", &N);
    for (int i = 1; i <= N; i++) {
        if (i % 2 == 0)
            sum -= i;
        else
            sum += i;
    }
    printf("Result: %d\n", sum);
    return 0;
}
```

11. **Sum of Series 12.2 + 22.3 + 32.4 + ...**
```c
#include <stdio.h>

int main() {
    int N;
    float sum = 0;
    scanf("%d", &N);
    for (int i = 1; i <= N; i++) {
        sum += i * 10 + 2 + i * 0.1;
    }
    printf("Result: %.1f\n", sum);
    return 0;
}
```

12. **Fibonacci Series up to N Terms**
```c
#include <stdio.h>

int main() {
    int N, a = 1, b = 1, temp;
    scanf("%d", &N);
    printf("%d", a);
    if (N > 1) {
        printf(", %d", b);
    }
    for (int i = 3; i <= N; i++) {
        temp = a + b;
        printf(", %d", temp);
        a = b;
        b = temp;
    }
    printf("\n");
    return 0;
}
```

13. **Factorial of N**
```c
#include <stdio.h>

int main() {
    int N, fact = 1;
    scanf("%d", &N);
    printf("%d! = ", N);
    for (int i = N; i > 0; i--) {
        fact *= i;
        printf("%d", i);
        if (i > 1)
            printf(" X ");
    }
    printf(" = %d\n", fact);
    return 0;
}
```

14. **Find nCr**
```c
#include <stdio.h>

int factorial(int n) {
    int fact = 1;
    for (int i = 2; i <= n; i++) {
        fact *= i;
    }
    return fact;
}

int main() {
    int n, r;
    scanf("%d %d", &n, &r);
    printf("%d\n", factorial(n) / (factorial(r) * factorial(n - r)));
    return 0;
}
```

15. **Find x^y**
```c
#include <stdio.h>

int main() {
    int x, y, result = 1;
    scanf("%d %d", &x, &y);
    for (int i = 0; i < y; i++) {
        result *= x;
    }
    printf("%d\n", result);
    return 0;
}
```

16. **Find GCD and LCM**
```c
#include <stdio.h>

int gcd(int a, int b) {
    while (b != 0) {
        int temp = b;
        b = a % b;
        a = temp;
    }
    return a;
}

int main() {
    int a, b;
    scanf("%d %d", &a, &b);
    int GCD = gcd(a, b);
    int LCM = (a * b) / GCD;
    printf("GCD: %d\nLCM: %d\n", GCD, LCM);
    return 0;
}
```

17. **Check Prime Number**
```c
#include <stdio.h>

int main() {
    int n, is_prime = 1;
    scanf("%d", &n);
    if (n <= 1)
        is_prime = 0;
    for (int i = 2; i <= n / 2; i++) {
        if (n % i == 0) {
            is_prime = 0;
            break;
        }
    }
    if (is_prime)
        printf("Prime\n");
    else
        printf("Not prime\n");
    return 0;
}
```

18. **Check Palindrome Number**
```c
#include <stdio.h>

int main() {
    int

 n, original, reversed = 0;
    scanf("%d", &n);
    original = n;
    while (n != 0) {
        reversed = reversed * 10 + n % 10;
        n /= 10;
    }
    if (original == reversed)
        printf("Yes\n");
    else
        printf("No\n");
    return 0;
}
```

19. **Calculate Mathematical Function**
```c
#include <stdio.h>
#include <math.h>

int main() {
    int x;
    scanf("%d", &x);
    printf("%.3f\n", sin(x));
    return 0;
}
```

20. **Sum of Series 1 + 12 + 123 + ...**
```c
#include <stdio.h>

int main() {
    int N, sum = 0, term = 0;
    scanf("%d", &N);
    for (int i = 1; i <= N; i++) {
        term = term * 10 + i;
        sum += term;
    }
    printf("%d\n", sum);
    return 0;
}
```
