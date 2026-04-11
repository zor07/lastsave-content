# lastsave-content — Структура и подходы

## Структура репозиториев

```
lastsave/
  lastsave-platform/    ← бот/бэкенд (Kotlin, Spring Boot, PostgreSQL)
  lastsave-infra/       ← docker-compose + GitHub Actions для деплоя
  lastsave-content/     ← теория в Markdown
  lastsave-templates/   ← шаблонные репо для студентов
```

---

## Контент (`lastsave-content`)

Иерархия: **блок → топик**. Один топик = одна лекция.

```
lastsave-content/
  content-plan.md       ← оглавление (единая точка истины по структуре)
  block1/
    topic1.md
    topic2.md
    ...
  block2/
    topic1.md
    ...
```

При добавлении нового блока или топика — сначала обновляем `content-plan.md`.

---

## Шаблонный репо студента (`lastsave-templates/student-template`)

Один репо на студента на весь период. Создаётся из шаблона при старте.

**Система сборки:** Maven  
**Java:** 21

**Структура пакетов:** `com.lastsave.blockNN.topicNN`

```
src/
  main/java/com/lastsave/
    block02/
      topic01/
      topic02/
      topic03/
  test/java/com/lastsave/
    block02/
      topic01/
      topic02/
      topic03/
```

**Формат задачи:**
- Класс с методами, тело которых нужно реализовать (`// TODO`)
- JUnit 5 тест рядом, проверяющий реализацию
- Тесты видны студенту — это намеренно

**Нейминг классов:** TBD — решим после того как увидим задачи.

---

## Ключевые решения

| Решение | Обоснование |
|---------|------------|
| 1 репо на студента (не на блок) | Удобнее студенту и преподавателю |
| Maven вместо Gradle | Проще для новичков |
| Пакеты по блоку + топику | Не запутаться при росте задач |
| Тесты видны студенту | Принимаем риски, избегаем оверхед с защитой |
| GitHub Classroom — отказались | Используем репо из шаблона напрямую |
