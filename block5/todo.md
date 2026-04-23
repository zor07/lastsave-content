# TODO — block5: ООП базово

## Подход к тестированию

Тесты используют рефлексию (`Class.forName`, `getDeclaredMethods`, `invoke`).
- Не требуют заглушек в шаблоне
- Компилируются без импорта класса студента
- Если класса нет — `ClassNotFoundException` в runtime
- Студент не обязан понимать как работают тесты

Структура пакетов: `block05.topicNN.taskNN` — каждая задача в своём пакете.

---

## topic1: Классы, объекты, поля, методы

1. Создай класс `Book` с полями `title`, `author`, `pages` и методом `getSummary()` → `"title by author, pages pages"`
2. Создай класс `Rectangle` с полями `width`, `height` и методами `area()`, `perimeter()`
3. Создай класс `Person` с полями `name`, `age` и методом `isAdult()` → `true` если >= 18

## topic2: Статика

1. Создай класс `Counter` со статическим полем `count` и методом `increment()`
2. Создай класс `MathUtils` со статическими методами `max(a, b)` и `min(a, b)`

## topic3: Модификаторы доступа

1. Создай класс `BankAccount` с приватным полем `balance`, методами `deposit(amount)` и `getBalance()`
2. Новый класс (придумать отдельно)

## topic4: Пакеты и import

— без задач с тестами, только теория

## topic5: Перегрузка методов

1. Создай класс `Printer` с тремя перегрузками `print` — для `int`, `double`, `String` (возвращают `String`)
2. Создай класс `Calculator` с перегрузками `add` — для двух и трёх аргументов
