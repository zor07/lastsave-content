# Naming Conventions

Соглашения об именовании — это негласный договор между разработчиками. Код читают люди, и правильные имена делают код понятным без комментариев.

В Java эти соглашения закреплены стандартом и соблюдаются повсеместно. Отступление от них — красный флаг на ревью.

---

## Классы — PascalCase

Каждое слово с заглавной буквы, без разделителей.

```java
// Правильно
class BankAccount { }
class UserProfileService { }
class HttpRequest { }

// Неправильно
class bankAccount { }    // первое слово строчное
class bank_account { }   // подчёркивание
class BANKACCOUNT { }    // всё заглавными
```

Имя класса — это существительное. Оно отвечает на вопрос «что это?».

---

## Методы и переменные — camelCase

Первое слово строчное, каждое следующее с заглавной буквы.

```java
// Методы
void sendMessage() { }
int calculateTotal() { }
boolean isUserActive() { }

// Переменные
int userAge = 25;
String firstName = "Alice";
boolean isLoggedIn = false;
```

Метод — это глагол или глагольная фраза: `get`, `set`, `calculate`, `send`, `is`, `has`.

Переменная — существительное или прилагательное + существительное.

---

## Константы — UPPER_SNAKE_CASE

Все буквы заглавные, слова разделяются подчёркиванием.

```java
static final int MAX_RETRY_COUNT = 3;
static final String DEFAULT_ENCODING = "UTF-8";
static final double PI = 3.14159;
```

Константа — это `static final` поле. Значение задаётся один раз и не меняется.

---

## Пакеты — строчные буквы, без подчёркиваний

```java
// Правильно
package com.lastsave.block02.topic01;

// Неправильно
package com.lastsave.Block02.Topic01;
package com.lastsave.block_02.topic_01;
```

---

## Имя файла = имя класса

Файл `BankAccount.java` должен содержать класс `BankAccount`. Это не просто соглашение — это требование компилятора для `public` классов.

---

## Зачем это важно

Плохие имена создают когнитивную нагрузку — читатель тратит время на расшифровку вместо понимания логики.

```java
// Что это делает?
int d = 86400;
boolean f(int x) { return x % 2 == 0; }

// Понятно без объяснений
int secondsInDay = 86400;
boolean isEven(int number) { return number % 2 == 0; }
```

Хорошее имя — это документация. Если метод называется `getUserById`, не нужно читать его тело чтобы понять что он делает.

---

## Шпаргалка

| Что | Стиль | Пример |
|-----|-------|--------|
| Класс | PascalCase | `OrderService` |
| Метод | camelCase | `calculatePrice()` |
| Переменная | camelCase | `itemCount` |
| Константа | UPPER_SNAKE_CASE | `MAX_SIZE` |
| Пакет | lowercase | `com.lastsave.block02` |
