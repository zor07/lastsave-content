# Установка JDK

JDK — это набор инструментов без которого Java-код не запустится. Установи его один раз и больше не трогай.

### Windows

1. Перейди на [adoptium.net](https://adoptium.net)
2. Нажми **Latest LTS release** — скачается установщик для Windows
3. Запусти `.msi` файл, все настройки оставь по умолчанию, жми Next до конца
4. Открой командную строку: `Win + R` → введи `cmd` → Enter
5. Введи команду и нажми Enter:
```
java -version
```
6. Ты должен увидеть строку вида `openjdk version "21.x.x"` — всё готово

### macOS

1. Перейди на [adoptium.net](https://adoptium.net)
2. Нажми **Latest LTS release** — скачается `.pkg` файл
3. Запусти его, все настройки по умолчанию
4. Открой Terminal (`Cmd + Space` → `Terminal`)
5. Введи:
```
java -version
```
6. Ты должен увидеть строку вида `openjdk version "21.x.x"` — всё готово

### Linux (Ubuntu / Debian)

1. Открой Terminal
2. Выполни по очереди:
```bash
sudo apt update
sudo apt install temurin-21-jdk
```
3. Проверь:
```bash
java -version
```
4. Ты должен увидеть строку вида `openjdk version "21.x.x"` — всё готово

> Если видишь другую версию или ошибку `command not found` — не двигайся дальше, напиши в чат поддержки.
