# Запуск Apache в Docker

## Цель работы
Научиться запускать готовый образ Apache в Docker, пробрасывать порты и монтировать локальную папку.

---

## Выполненные шаги

### 1. Запуск контейнера Apache

```bash
docker run -d --name my-apache -p 8080:80 httpd:latest
```

---

### 2. Проверка работы контейнера

Команда `docker ps` показывает запущенный контейнер:

```bash
docker ps
```

![docker ps](../screenshots/docker-ps.png)

---

### 3. Страница Apache по умолчанию

По адресу `http://localhost:8080` открылась страница "It works!":

![Apache default](../screenshots/apache-default.png)

---

### 4. Создание своей веб-страницы

Создал файл `website/index.html` с содержимым:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Мой сайт на Docker</title>
</head>
<body>
    <h1>Мой сайт на Apache в Docker</h1>
    <p>Это моя первая страница, работающая в контейнере</p>
    <hr>
    <small>Работает на Apache в Docker</small>
</body>
</html>
```

---

### 5. Запуск с монтированием папки

```bash
docker stop my-apache
docker rm my-apache
docker run -d --name my-apache -p 8080:80 -v C:\Users\Evg65\Desktop\docker-projects\website:/usr/local/apache2/htdocs/ httpd:latest
```

---

### 6. Проверка монтирования

```bash
docker exec my-apache ls -la /usr/local/apache2/htdocs/
```

**Результат:**

```
total 8
drwxrwxrwx 1 root     root     4096 Mar 24 08:46 .
drwxr-xr-x 1 www-data www-data 4096 Mar 16 22:22 ..
-rwxrwxrwx 1 root     root      365 Mar 24 08:49 index.html
```

---

### 7. Проверка содержимого файла

```bash
docker exec my-apache cat /usr/local/apache2/htdocs/index.html
```

---

### 8. Результат

После обновления страницы появилась моя кастомная страница:

![Custom page](../screenshots/apache-custom.png)

---

## Вывод

Я успешно запустил веб-сервер Apache в Docker, научился пробрасывать порты и подключать локальные файлы. Контейнер работает, моя страница отображается в браузере.

---

## Полезные команды

| Команда | Описание |
|---------|----------|
| `docker ps` | Показать запущенные контейнеры |
| `docker stop my-apache` | Остановить контейнер |
| `docker start my-apache` | Запустить контейнер |
| `docker logs my-apache` | Посмотреть логи |
| `docker exec my-apache ls /usr/local/apache2/htdocs/` | Проверить файлы в контейнере |
```

---

## Файл 2: `README.md` (корень репозитория)

```markdown
# Мои Docker-проекты

Этот репозиторий содержит мои работы по изучению Docker.

---

## Выполненные задания

| № | Задание | Описание | Отчет |
|---|---------|----------|-------|
| 1 | **Apache** | Запуск веб-сервера Apache в Docker | [Apache.md](myNotes/Apache.md) |

---

## Структура репозитория

```
docker-projects/
├── myNotes/
│   └── Apache.md
├── screenshots/
│   ├── docker-ps.png
│   ├── apache-default.png
│   └── apache-custom.png
├── website/
│   └── index.html
└── README.md
```

---

## Как запустить Apache

```bash
# Запуск контейнера
docker run -d --name my-apache -p 8080:80 httpd:latest

# Остановка и удаление
docker stop my-apache
docker rm my-apache

# Запуск с монтированием локальной папки
docker run -d --name my-apache -p 8080:80 -v C:\Users\Evg65\Desktop\docker-projects\website:/usr/local/apache2/htdocs/ httpd:latest
```

---

## Полезные команды Docker

| Команда | Описание |
|---------|----------|
| `docker ps` | Показать запущенные контейнеры |
| `docker ps -a` | Показать все контейнеры |
| `docker stop <name>` | Остановить контейнер |
| `docker rm <name>` | Удалить контейнер |
| `docker logs <name>` | Посмотреть логи |
| `docker exec <name> <command>` | Выполнить команду в контейнере |

---

*Репозиторий обновляется по мере выполнения новых заданий.*
```

---

Всё. Копируйте каждый блок в соответствующий файл и сохраняйте.