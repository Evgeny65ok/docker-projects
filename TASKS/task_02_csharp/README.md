# Задание 2: C# .NET в Docker

## Описание
Веб-приложение на ASP.NET Core, запущенное в Docker контейнере.

## Файлы проекта
- `Program.cs` - код приложения
- `MyApp.csproj` - файл проекта
- `Dockerfile` - инструкции для сборки

## Команды

### Сборка образа
```bash
docker build -t my-dotnet-app .
```

### Запуск контейнера
```bash
docker run -d --name my-dotnet-container -p 8081:80 my-dotnet-app
```

### Проверка
Открыть в браузере: http://localhost:8081

## Скриншот
<img width="360" height="162" alt="image" src="https://github.com/user-attachments/assets/29e62249-2d5e-48fc-9337-a94746ba15f8" />


---
*Выполнено: Евгений*
