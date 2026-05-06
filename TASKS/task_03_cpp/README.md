# Задание 3: C++ Console в Docker

## Описание
Консольное приложение на C++, которое выводит "Hello, Docker! from C++"

## Файлы проекта
- `hello.cpp` - исходный код
- `Dockerfile` - двухэтапная сборка (gcc → alpine)

## Команды

### Сборка образа
```bash
docker build -t cpp-hello .
```

### Запуск контейнера
```bash
docker run --rm cpp-hello
```

### Войти в контейнер для исследования
```bash
docker run -it --entrypoint sh cpp-hello
```

## Скриншот
<img width="668" height="179" alt="image" src="https://github.com/user-attachments/assets/e61ac424-f7d1-4d29-af7a-d21f4b3ebd65" />


---
*Выполнено: Евгений*
