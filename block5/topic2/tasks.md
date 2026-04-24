# Задачи — Статические поля и методы

В этом разделе задачи на статику. Каждая задача — в своём пакете (папке).

Найди папку `com/lastsave/block05/topic02` — внутри неё четыре папки: `task01`, `task02`, `task03`, `task04`. В каждой папке есть файл `package-info.java` — трогать его не нужно, это маркер для навигации.

**Важно:** соблюдай названия классов, полей и методов из условия — тесты проверяют по именам.

**Важно:** поля объявляй без модификатора доступа, методы — с `public`. Статические поля и методы объявляй с ключевым словом `static`.

---

### Задача 1. Счётчик

**Пакет:** `com.lastsave.block05.topic02.task01`

Создай класс `Counter`.

У него нет полей объекта. Есть одно статическое поле:
- `count` — целое число, изначально `0`

Добавь методы:
- `increment()` — увеличивает `count` на 1, ничего не возвращает
- `getCount()` — возвращает текущее значение `count`

Важно: `count` — статическое поле, оно одно на весь класс. Сколько бы объектов `Counter` ты ни создал — счётчик у них общий.

Пример:

```java
Counter c1 = new Counter();
Counter c2 = new Counter();

c1.increment();
c1.increment();
c2.increment();

System.out.println(Counter.getCount()); // 3
```

---

### Задача 2. Общий ресурс

**Пакет:** `com.lastsave.block05.topic02.task02`

Создай класс `BankAccount`, который описывает банковский аккаунт.

Поля:
- `balance` — баланс конкретного аккаунта (`int`)
- `bankTotalMoney` — статическое поле, общая сумма всех денег в банке (`int`), изначально `0`

Добавь конструктор, принимающий начальный `balance`. При создании аккаунта `bankTotalMoney` должен увеличиться на переданный баланс.

Добавь метод:
- `deposit(int amount)` — пополняет баланс аккаунта и одновременно увеличивает `bankTotalMoney`

Пример:

```java
BankAccount acc1 = new BankAccount(100);
BankAccount acc2 = new BankAccount(200);

System.out.println(BankAccount.bankTotalMoney); // 300

acc1.deposit(50);

System.out.println(acc1.balance);               // 150
System.out.println(BankAccount.bankTotalMoney); // 350
```

---

### Задача 3. Подсчёт объектов

**Пакет:** `com.lastsave.block05.topic02.task03`

Создай класс `Person`.

Поля объекта:
- `name` — имя (`String`)
- `age` — возраст (`int`)

Статическое поле:
- `count` — количество созданных объектов `Person`, изначально `0`

Добавь конструктор, принимающий `name` и `age`. При каждом создании нового объекта `count` должен увеличиваться на 1.

Пример:

```java
System.out.println(Person.count); // 0

Person p1 = new Person("Alex", 25);
Person p2 = new Person("Maria", 30);

System.out.println(Person.count); // 2
```

---

### Задача 4. Генератор идентификаторов

**Пакет:** `com.lastsave.block05.topic02.task04`

Создай два класса: `IdGenerator` и `Order`.

**Класс `IdGenerator`:**

Статическое поле:
- `lastId` — последний выданный id (`int`), изначально `0`

Статический метод:
- `nextId()` — увеличивает `lastId` на 1 и возвращает новое значение

**Класс `Order`:**

Поле:
- `id` — уникальный идентификатор заказа (`int`)

Добавь конструктор без параметров. При создании каждого объекта `Order` его поле `id` должно получать значение из `IdGenerator.nextId()`.

Пример:

```java
Order o1 = new Order();
Order o2 = new Order();
Order o3 = new Order();

System.out.println(o1.id); // 1
System.out.println(o2.id); // 2
System.out.println(o3.id); // 3
```
