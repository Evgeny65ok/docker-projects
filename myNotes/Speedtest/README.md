
# Задание №4: Speedtest

## Цель работы
Запустить тест скорости интернета в Docker контейнере

## Выполнение

### 1. Запуск контейнера
```
docker run -d -p 158:80 --name speedtest-server adolfintel/speedtest
```

### 2. Проверка работы
```
docker ps
```

![docker ps](../../screenshots/speedtest/docker-ps.png)

### 3. Открытие в браузере
http://localhost:158

![speedtest page](../../screenshots/speedtest/speedtest-page.png)

### 4. Запуск теста скорости

![speedtest running](../../screenshots/speedtest/speedtest-running.png)

### 5. Результат теста

![speedtest result](../../screenshots/speedtest/speedtest-result.png)

## Возможности Speedtest

- Проверка скорости загрузки (Download)
- Проверка скорости отдачи (Upload)
- Измерение пинга (Ping)
- Веб-интерфейс для запуска тестов

## Вывод
Speedtest запущен и доступен по адресу http://localhost:158
```
