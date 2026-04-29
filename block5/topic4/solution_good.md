# Хорошее решение — Пакеты и импорты

## Класс Person

```java
package com.lastsave.block05.topic04.task01.persons;

public class Person {
    private String name;
    private String city;

    public Person(String name, String city) {
        this.name = name;
        this.city = city;
    }

    public String getName() {
        return name;
    }

    public String getCity() {
        return city;
    }
}
```

## Класс PersonParser

```java
package com.lastsave.block05.topic04.task01.persons;

public class PersonParser {

    public Person parse(String input) {
        String[] parts = input.split(", ");
        if (parts.length != 2) {
            return null;
        }
        return new Person(parts[0], parts[1]);
    }
}
```

## Класс PersonValidator

```java
package com.lastsave.block05.topic04.task01.persons;

public class PersonValidator {

    public static boolean validate(String input) {
        return input.split(", ").length == 2;
    }
}
```

---

**Почему это хорошее решение:**

- Поля `name` и `city` объявлены `private` — данные защищены, доступ только через геттеры.
- `PersonParser` не смешивает логику парсинга с моделью — каждый класс отвечает за своё.
- `PersonValidator.validate` — статический, как и требовалось: он не зависит от состояния объекта.
- Возврат `null` при некорректном формате — простой и понятный контракт.
