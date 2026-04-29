# Плохое решение — Пакеты и импорты

## Класс Person

```java
package com.lastsave.block05.topic04.task01.persons;

public class Person {
    public String name;  // ❌ поля публичные — любой может изменить напрямую
    public String city;

    public Person(String name, String city) {
        this.name = name;
        this.city = city;
    }

    // геттеров нет — тесты упадут
}
```

## Класс PersonParser со встроенной валидацией

```java
package com.lastsave.block05.topic04.task01.persons;

public class PersonParser {

    public Person parse(String input) {
        // ❌ логика валидации продублирована внутри парсера
        // PersonValidator существует отдельно именно чтобы этого не делать
        if (input == null || !input.contains(", ")) {
            return null;
        }
        String[] parts = input.split(", ");
        // ❌ не проверяем что частей ровно две — "a, b, c" пройдёт
        return new Person(parts[0], parts[1]);
    }
}
```

## Класс PersonValidator с нестатическим методом

```java
package com.lastsave.block05.topic04.task01.persons;

public class PersonValidator {

    // ❌ метод не статический, хотя не использует никакого состояния объекта
    // PersonValidator validator = new PersonValidator() — лишний объект без смысла
    public boolean validate(String input) {
        return input.contains(", ");  // ❌ "a, b, c" тоже пройдёт валидацию
    }
}
```

---

**Типичные ошибки:**

- Публичные поля вместо `private` + геттеры — нарушение инкапсуляции.
- Дублирование логики: валидация внутри парсера и отдельно в `PersonValidator` — два места, которые могут разойтись.
- Проверка `contains(", ")` вместо `split(", ").length == 2` — не отлавливает строки с тремя и более частями.
- Нестатический `validate` — метод не использует поля объекта, но заставляет создавать экземпляр.
