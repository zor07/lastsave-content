```java
package com.lastsave.block02.topic01;

public class QuestB2T1 {

    public int sum(int a, int b) {
        return a + b;
    }

    public int minutesFromSeconds(int seconds) {
        return seconds / 60;
    }

    public boolean isEven(int number) {
        return number % 2 == 0;
    }

    public double celsiusToFahrenheit(double celsius) {
        return celsius * 9.0 / 5 + 32;
    }

    public boolean isAdult(int age) {
        return age >= 18;
    }

    public int max(int a, int b) {
        return a > b ? a : b;
    }

    public int absValue(int n) {
        return n < 0 ? -n : n;
    }

    public boolean isInRange(int value, int min, int max) {
        return value >= min && value <= max;
    }

    public double average(int a, int b) {
        return (a + b) / 2.0;
    }

    public int hoursFromSeconds(int seconds) {
        return seconds / 3600;
    }
}
```
