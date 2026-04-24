# Класс String — основы

В Java строка — это объект класса `String`. В отличие от примитивов, у строк есть богатая встроенная функциональность: поиск подстрок, изменение регистра, сравнение содержимого и многое другое.

В этой теме разберём как создавать строки и познакомимся с основными методами класса `String`.

## Создание строки

Большинство объектов в Java создаётся через `new`:

```java
Cat cat = new Cat();
Date date = new Date();
```

Для `String` это необязательно — можно просто написать строковый литерал:

```java
String name = "Java";
String empty = "";
```

Технически `new` тоже работает:

```java
String name = new String("Java");
```

Но на практике так не делают — литерал короче и эффективнее. Почему именно так устроено — разберём в следующей теме, пока просто запомни.

А сейчас перейдём к основным методам класса `String`.

## Длина строки

```java
String s = "Hello";
int len = s.length(); // 5
```

## Доступ к символу

```java
String s = "Hello";
char first = s.charAt(0);              // 'H'
char last  = s.charAt(s.length() - 1); // 'o'
```

## Поиск

```java
String s = "Hello";
s.contains("ell");     // true
s.indexOf("l");        // 2 — первое вхождение
s.lastIndexOf("l");    // 3 — последнее вхождение
s.startsWith("He");    // true
s.endsWith("lo");      // true
```

## Подстрока

```java
String s = "Hello";
s.substring(1);     // "ello" — от индекса до конца
s.substring(1, 3);  // "el"  — от 1 включительно до 3 не включительно
```

## Регистр

```java
String s = "Hello";
s.toUpperCase(); // "HELLO"
s.toLowerCase(); // "hello"
```

## Пробелы

```java
String s = "  hello  ";
s.trim();  // "hello" — убирает пробелы по краям
s.strip(); // "hello" — современный вариант, понимает Unicode-пробелы
```

## Замена

```java
String s = "Hello";
s.replace('l', 'r');     // "Herro"
s.replace("ell", "ELL"); // "HELLo"
```

## Сравнение

```java
String a = "hello";
String b = "HELLO";

a.equals(b);           // false — регистр важен
a.equalsIgnoreCase(b); // true  — регистр не важен
```

> `==` сравнивает не содержимое, а ссылки. Для сравнения строк всегда используй `equals`.

## Пустая строка

```java
String s = "";
s.isEmpty();           // true

String spaces = "  ";
spaces.isEmpty();      // false — есть пробелы
spaces.isBlank();      // true  — только пробельные символы
```

## Преобразование

```java
String s = String.valueOf(42);  // "42"
int n = Integer.parseInt("42"); // 42
```

> Если передать строку, которая не является числом — программа упадёт с ошибкой:
> ```java
> int n = Integer.parseInt("abc"); // ошибка во время выполнения
> ```
> Про ошибки и как с ними работать поговорим отдельно, пока просто будь внимательным.
