# Задание №2: Welcome to Docker

## Цель работы
Запустить демонстрационный контейнер docker/welcome-to-docker

## Выполнение

### 1. Запуск контейнера
```
docker run -d -p 8088:80 --name welcome-to-docker docker/welcome-to-docker
```

### 2. Проверка работы
```
docker ps
```

![docker ps](../../screenshots/screenshotswelcome/docker-ps.png)

### 3. Веб-интерфейс
http://localhost:8088

![welcome page](../../screenshots/screenshotswelcome/welcome-page.png)

### 4. Вход в контейнер
```
docker exec -it welcome-to-docker /bin/sh
```

### 5. Информация о системе
```
uname -a
```

![uname](../../screenshots/screenshotswelcome/uname.png)

### 6. Обновление пакетов
```
apk update && apk upgrade
```

![apk update](../../screenshots/screenshotswelcome/apk-update.png)

### 7. Установка fastfetch
```
apk add fastfetch
```

![apk add](../../screenshots/screenshotswelcome/apk-add.png)

### 8. Запуск fastfetch
```
fastfetch
```

![fastfetch](../../screenshots/screenshotswelcome/fastfetch.png)

### 9. Выход
```
exit
```

### 10. Остановка контейнера
```
docker stop welcome-to-docker
```

## Вывод
Задание выполнено. Контейнер запущен, порт проброшен, команды внутри отработали.
```

**Всё, копируй, вставляй, сохраняй, пуш на GitHub.**

**Пиши "погнали к третьему"** 🚀