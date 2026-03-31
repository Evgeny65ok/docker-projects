📄 Вот финальный код для myNotes/MySQL/README.md:
markdown
# Задание №6: MySQL база данных

## Цель работы
Запустить MySQL в Docker контейнере

## Выполнение

### 1. Запуск контейнера
docker run -d
--name my-mysql
-p 3306:3306
-e MYSQL_ROOT_PASSWORD=rootpassword
-e MYSQL_DATABASE=mydb
-e MYSQL_USER=user
-e MYSQL_PASSWORD=password
mysql:8

text

### 2. Проверка работы
docker ps

text

![docker ps](../../screenshots/mysql/docker-ps.png)

### 3. Подключение к MySQL
docker exec -it my-mysql mysql -u root -p

text
Пароль: rootpassword

### 4. Список баз данных
```sql
SHOW DATABASES;
https://../../screenshots/mysql/mysql-databases.png

5. Версия MySQL
sql
SELECT VERSION();
https://../../screenshots/mysql/mysql-version.png

6. Создание таблицы
sql
USE mydb;
CREATE TABLE test (id INT, name VARCHAR(50));
SHOW TABLES;
https://../../screenshots/mysql/mysql-createtable.png

Вывод
MySQL запущен и доступен через порт 3306

text

## 🚀 Сохрани и отправь:

```bash
git add myNotes/MySQL/README.md
git commit -m "fix mysql paths - final"
git push
Теперь точно будет работать. Пиши "погнали к седьмому" 🚀

