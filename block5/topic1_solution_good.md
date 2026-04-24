```java
package com.lastsave.block05.topic01.task01;

public class Book {
    String title;
    String author;
    int pages;

    public Book(String title, String author, int pages) {
        this.title = title;
        this.author = author;
        this.pages = pages;
    }

    public String getSummary() {
        return title + " by " + author + ", " + pages + " pages";
    }
}
```

```java
package com.lastsave.block05.topic01.task02;

public class Rectangle {
    int width;
    int height;

    public Rectangle() {
        this.width = 1;
        this.height = 1;
    }

    public Rectangle(int width, int height) {
        this.width = width;
        this.height = height;
    }

    public int area() {
        return width * height;
    }

    public int perimeter() {
        return 2 * (width + height);
    }
}
```

```java
package com.lastsave.block05.topic01.task03;

public class Person {
    String name;
    int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public boolean isAdult() {
        return age >= 18;
    }
}
```
