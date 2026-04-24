```java
// task01 — count не статическое, у каждого объекта своё
package com.lastsave.block05.topic02.task01;

public class Counter {
    int count = 0; // не static — каждый объект хранит свой счётчик

    public void increment() {
        count++;
    }

    public static int getCount() {
        return 0; // не может вернуть count — он не статический
    }
}
```

```java
// task02 — bankTotalMoney не обновляется при deposit
package com.lastsave.block05.topic02.task02;

public class BankAccount {
    int balance;
    static int bankTotalMoney = 0;

    public BankAccount(int balance) {
        this.balance = balance;
        bankTotalMoney += balance;
    }

    public void deposit(int amount) {
        balance += amount; // bankTotalMoney не обновляется
    }
}
```

```java
// task03 — count не инкрементируется в конструкторе
package com.lastsave.block05.topic02.task03;

public class Person {
    String name;
    int age;
    static int count = 0;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
        // забыли count++
    }
}
```

```java
// task04 — nextId не инкрементирует перед возвратом, первый id будет 0
package com.lastsave.block05.topic02.task04;

public class IdGenerator {
    static int lastId = 0;

    public static int nextId() {
        return lastId++; // сначала возвращает, потом инкрементирует
    }
}
```

```java
// task04 — Order корректный
package com.lastsave.block05.topic02.task04;

public class Order {
    int id;

    public Order() {
        this.id = IdGenerator.nextId();
    }
}
```
