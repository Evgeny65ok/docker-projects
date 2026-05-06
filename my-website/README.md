# Статический сайт на Nginx в Docker

## Описание
Веб-сервер Nginx с простой HTML-страницей.

## Команды

### Сборка образа
```bash
docker build -t my-site .
```

### Запуск контейнера
```bash
docker run -d -p 8081:80 --name my-site -v $(pwd):/usr/share/nginx/html my-site
```

### Проверка
Открыть в браузере: http://localhost:8081

## Скриншот
<img width="547" height="183" alt="image" src="https://github.com/user-attachments/assets/987bc747-62b3-4bb8-ab63-a46e8282c201" />


---
*Выполнено: Евгений*
