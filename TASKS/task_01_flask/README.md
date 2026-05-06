# Задание 1: Flask + Python в Docker

## Описание
Веб-приложение на Flask, запущенное в Docker контейнере.

## Файлы проекта
- `app.py` - код приложения
- `requirements.txt` - зависимости
- `Dockerfile` - инструкции для сборки

## Команды

### Сборка образа
```bash
docker build -t my-flask-app .
```

### Запуск контейнера
```bash
docker run -d --name my-flask-container -p 8082:5000 my-flask-app
```

### Проверка
Открыть в браузере: http://localhost:8082

## Скриншот
<img width="367" height="192" alt="image" src="https://github.com/user-attachments/assets/2e430936-0de8-462a-8339-141bec4716e7" />


---
*Выполнено: Евгений*
