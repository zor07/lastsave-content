```java
// task01
package com.lastsave.block05.topic05.task01;

public class Logger {

    public String log(String message) {
        return "[INFO] " + message;
    }

    public String log(String message, String level) {
        return "[" + level + "] " + message;
    }

    public String log(String message, String level, String time) {
        return "[" + level + "] " + time + " " + message;
    }
}
```

```java
// task02
package com.lastsave.block05.topic05.task02;

public class Calculator {

    public int add(int a, int b) {
        return a + b;
    }

    public int add(int a, int b, int c) {
        return a + b + c;
    }

    public double add(double a, double b) {
        return a + b;
    }
}
```
