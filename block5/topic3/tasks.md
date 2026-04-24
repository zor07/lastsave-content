# Задачи — Модификаторы доступа, геттеры, сеттеры

Найди папку `com/lastsave/block05/topic03` — внутри неё две папки: `task01` и `task02`. В каждой папке есть файл `Main.java` — в нём можно запустить и проверить свой код вручную. Создавай свои классы в той же папке что и `Main.java`.

**Важно:** соблюдай названия классов, полей и методов из условия — тесты проверяют по именам.

**Важно:** все поля объявляй с модификатором `private`, все методы — с `public`.

---

### Задача 1. Класс Product

**Пакет:** `com.lastsave.block05.topic03.task01`

Создай класс `Product`, который описывает товар.

Поля (оба приватные):
- `name` — название товара (`String`)
- `price` — цена (`double`)

Добавь конструктор, принимающий оба поля.

Добавь геттеры:
- `getName()` — возвращает название
- `getPrice()` — возвращает цену

Добавь сеттер для цены:
- `setPrice(double price)` — устанавливает цену. Если переданное значение отрицательное — ничего не делать и завершить метод.

Пример:

```java
Product p = new Product("Laptop", 1500.0);
System.out.println(p.getName());  // Laptop
System.out.println(p.getPrice()); // 1500.0

p.setPrice(-100);
System.out.println(p.getPrice()); // 1500.0 — цена не изменилась

p.setPrice(2000.0);
System.out.println(p.getPrice()); // 2000.0
```

---

### Задача 2. Класс Student

**Пакет:** `com.lastsave.block05.topic03.task02`

Создай класс `Student`, который описывает студента.

Поля (оба приватные):
- `name` — имя (`String`)
- `grade` — оценка (`int`)

Добавь конструктор, принимающий оба поля.

Добавь геттеры:
- `getName()` — возвращает имя
- `getGrade()` — возвращает оценку

Добавь сеттер для оценки:
- `setGrade(int grade)` — устанавливает оценку. Если переданное значение меньше 1 или больше 5 — ничего не делать и завершить метод.

Пример:

```java
Student s = new Student("Alex", 4);
System.out.println(s.getName());  // Alex
System.out.println(s.getGrade()); // 4

s.setGrade(10);
System.out.println(s.getGrade()); // 4 — некорректная оценка не прошла

s.setGrade(5);
System.out.println(s.getGrade()); // 5
```
