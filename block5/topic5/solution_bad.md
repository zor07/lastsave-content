```java
// task01 — разные имена методов вместо перегрузки, неверный порядок в третьей перегрузке
package com.lastsave.block05.topic05.task01;

public class Logger {

    public String logDefault(String message) { // отдельное имя — не перегрузка
        return "[INFO] " + message;
    }

    public String log(String message, String level) {
        return "[" + level + "] " + message;
    }

    public String log(String message, String level, String time) {
        return "[" + level + "] " + message + " " + time; // message и time перепутаны местами
    }
}
```

```java
// task02 — перегрузка по имени параметра (не работает), отсутствует перегрузка для double
package com.lastsave.block05.topic05.task02;

public class Calculator {

    public int add(int a, int b) {
        return a + b;
    }

    public int add(int x, int y) { // ошибка компиляции — сигнатура та же, имена параметров не считаются
        return x + y;
    }

    // перегрузка для double отсутствует
}
```
