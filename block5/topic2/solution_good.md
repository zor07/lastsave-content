```java
// task01
package com.lastsave.block05.topic02.task01;

public class Counter {
    static int count = 0;

    public void increment() {
        count++;
    }

    public static int getCount() {
        return count;
    }
}
```

```java
// task02
package com.lastsave.block05.topic02.task02;

public class BankAccount {
    int balance;
    static int bankTotalMoney = 0;

    public BankAccount(int balance) {
        this.balance = balance;
        bankTotalMoney += balance;
    }

    public void deposit(int amount) {
        balance += amount;
        bankTotalMoney += amount;
    }
}
```

```java
// task03
package com.lastsave.block05.topic02.task03;

public class Person {
    String name;
    int age;
    static int count = 0;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
        count++;
    }
}
```

```java
// task04 — IdGenerator
package com.lastsave.block05.topic02.task04;

public class IdGenerator {
    static int lastId = 0;

    public static int nextId() {
        return ++lastId;
    }
}
```

```java
// task04 — Order
package com.lastsave.block05.topic02.task04;

public class Order {
    int id;

    public Order() {
        this.id = IdGenerator.nextId();
    }
}
```
