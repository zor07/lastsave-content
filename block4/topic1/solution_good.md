```java
package com.lastsave.block04.topic01;

public class QuestB4T1 {

    public int getFirstEven(int[] numbers) {
        for (int n : numbers) {
            if (n % 2 == 0) return n;
        }
        return 0;
    }

    public int getLast(int[] numbers) {
        if (numbers.length == 0) return 0;
        return numbers[numbers.length - 1];
    }

    public int sum(int[] numbers) {
        int sum = 0;
        for (int n : numbers) sum += n;
        return sum;
    }

    public int min(int[] numbers) {
        int min = numbers[0];
        for (int n : numbers) {
            if (n < min) min = n;
        }
        return min;
    }

    public double average(int[] numbers) {
        int sum = 0;
        for (int n : numbers) sum += n;
        return (double) sum / numbers.length;
    }

    public boolean contains(int[] numbers, int target) {
        for (int n : numbers) {
            if (n == target) return true;
        }
        return false;
    }

    public int countEven(int[] numbers) {
        int count = 0;
        for (int n : numbers) {
            if (n % 2 == 0) count++;
        }
        return count;
    }

    public int sumEven(int[] numbers) {
        int sum = 0;
        for (int n : numbers) {
            if (n % 2 == 0) sum += n;
        }
        return sum;
    }

    public int[] reverse(int[] numbers) {
        int[] result = new int[numbers.length];
        for (int i = 0; i < numbers.length; i++) {
            result[i] = numbers[numbers.length - 1 - i];
        }
        return result;
    }

    public int[] copy(int[] numbers) {
        int[] result = new int[numbers.length];
        for (int i = 0; i < numbers.length; i++) {
            result[i] = numbers[i];
        }
        return result;
    }
}
```
