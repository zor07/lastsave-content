```java
// task01 — добавлен лишний setName, валидация отсутствует
package com.lastsave.block05.topic03.task01;

public class Product {
    private String name;
    private double price;

    public Product(String name, double price) {
        this.name = name;
        this.price = price;
    }

    public String getName() {
        return name;
    }

    public double getPrice() {
        return price;
    }

    public void setName(String name) { // лишний сеттер — name не должен меняться
        this.name = name;
    }

    public void setPrice(double price) {
        this.price = price; // нет валидации — отрицательная цена пройдёт
    }
}
```

```java
// task02 — валидация неполная, лишний сеттер для name
package com.lastsave.block05.topic03.task02;

public class Student {
    private String name;
    private int grade;

    public Student(String name, int grade) {
        this.name = name;
        this.grade = grade;
    }

    public String getName() {
        return name;
    }

    public int getGrade() {
        return grade;
    }

    public void setName(String name) { // лишний сеттер — name не должен меняться
        this.name = name;
    }

    public void setGrade(int grade) {
        if (grade < 1) return; // проверяет только нижнюю границу, верхняя не проверяется
        this.grade = grade;
    }
}
```
