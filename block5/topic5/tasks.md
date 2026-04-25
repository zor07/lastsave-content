# Задачи — Перегрузка методов

Найди пакет `com.lastsave.block05.topic05` — внутри две папки: `task01` и `task02`. В каждой есть `Main.java` для ручной проверки.

**Важно:** соблюдай названия классов и методов из условия — тесты проверяют по именам.

---

### Задача 1. Класс Logger

**Пакет:** `com.lastsave.block05.topic05.task01`

Создай класс `Logger` с тремя перегрузками метода `log`. Все методы возвращают `String` — отформатированную строку, а не печатают её в консоль.

- `log(String message)` — уровень по умолчанию `INFO`, возвращает строку вида: `[INFO] message`
- `log(String message, String level)` — уровень передаётся явно, возвращает строку вида: `[level] message`
- `log(String message, String level, String time)` — уровень и время передаются явно, возвращает строку вида: `[level] time message`

Пример:

```java
Logger logger = new Logger();

System.out.println(logger.log("Сервер запущен"));
// [INFO] Сервер запущен

System.out.println(logger.log("Ошибка подключения", "ERROR"));
// [ERROR] Ошибка подключения

System.out.println(logger.log("Пользователь вошёл", "INFO", "10:42"));
// [INFO] 10:42 Пользователь вошёл
```

---

### Задача 2. Класс Calculator

**Пакет:** `com.lastsave.block05.topic05.task02`

Создай класс `Calculator` с тремя перегрузками метода `add`:

- `add(int a, int b)` — возвращает сумму двух целых чисел
- `add(int a, int b, int c)` — возвращает сумму трёх целых чисел
- `add(double a, double b)` — возвращает сумму двух дробных чисел

Пример:

```java
Calculator calc = new Calculator();

System.out.println(calc.add(2, 3));       // 5
System.out.println(calc.add(2, 3, 4));    // 9
System.out.println(calc.add(1.5, 2.5));   // 4.0
```
