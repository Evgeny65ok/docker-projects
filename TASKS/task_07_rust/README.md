# Задание 7: Приложение на Rust

## Описание
Консольное приложение на Rust, которое выводит "Hello from Rust inside Docker! 🦀"

## Файлы проекта
- `src/main.rs` - исходный код
- `Cargo.toml` - конфигурация проекта
- `Dockerfile` - двухэтапная сборка

## Команды

### Сборка образа
```bash
docker build -t rust-app .
```

### Запуск контейнера
```bash
docker run -it --rm rust-app
```

### Войти в контейнер для исследования
```bash
docker run -it --rm --entrypoint sh rust-app
./rust-app
```

## Скриншот
<img width="741" height="69" alt="image" src="https://github.com/user-attachments/assets/dd9e81f9-d1fd-4ea7-bf68-96b64eb86495" />


---
*Выполнено: Евгений*
