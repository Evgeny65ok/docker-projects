# Задание 5: Wow - консольное псевдографическое приложение на C++ и FTXUI

## Описание
Консольное приложение с анимированным gauge (индикатором прогресса) на C++ с использованием библиотеки FTXUI.

## Файлы проекта
- `main.cpp` - исходный код с анимацией
- `CMakeLists.txt` - сборка через CMake
- `Dockerfile` - двухэтапная сборка

## Команды

### Сборка образа
```bash
docker build -t ftxui-wow .
```

### Запуск контейнера
```bash
docker run -it --rm ftxui-wow
```

### Войти в контейнер для исследования
```bash
docker run -it --entrypoint bash ftxui-wow
```

## Скриншот

<img width="994" height="248" alt="image" src="https://github.com/user-attachments/assets/918a6049-8ebf-46d3-8256-23ed44c991db" />


---
*Выполнено: Евгений*
