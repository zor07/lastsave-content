```java
package com.lastsave.block02.topic02;

public class QuestB2T2 {

    public String getGrade(int score) {
        if (score >= 90) return "Отлично";
        if (score >= 70) return "Хорошо";
        if (score >= 50) return "Удовлетворительно";
        return "Неудовлетворительно";
    }

    public int sumUpTo(int n) {
        int sum = 0;
        for (int i = 1; i <= n; i++) {
            sum += i;
        }
        return sum;
    }

    public int factorial(int n) {
        int result = 1;
        for (int i = 2; i <= n; i++) result *= i;
        return result;
    }

    public boolean isPrime(int n) {
        if (n < 2) return false;
        for (int i = 2; i * i <= n; i++) {
            if (n % i == 0) return false;
        }
        return true;
    }

    public int countDigits(int n) {
        if (n == 0) return 1;
        return String.valueOf(Math.abs(n)).length();
    }

    public int sumEven(int n) {
        int sum = 0;
        for (int i = 2; i <= n; i += 2) sum += i;
        return sum;
    }

    public int power(int base, int exponent) {
        int result = 1;
        for (int i = 0; i < exponent; i++) result *= base;
        return result;
    }

    public int gcd(int a, int b) {
        while (b != 0) { int t = b; b = a % b; a = t; }
        return a;
    }

    public int sumOfDigits(int n) {
        int sum = 0;
        n = Math.abs(n);
        while (n > 0) { sum += n % 10; n /= 10; }
        return sum;
    }

    public int fibonacci(int n) {
        if (n == 0) return 0;
        int a = 0, b = 1;
        for (int i = 2; i <= n; i++) { int c = a + b; a = b; b = c; }
        return b;
    }
}
```
