Скриншоты не видны, потому что у тебя в README.md **нет синтаксиса markdown для вставки картинок**.

Ты написал просто текст:
```
Скриншот: screenshots/cadvisor/docker-ps.png
```

А нужно писать так:
```markdown
![docker ps](screenshots/cadvisor/docker-ps.png)
```

## 🔧 Вот исправленный код. Скопируй его полностью и вставь в файл `myNotes/cAdvisor/README.md`:

```markdown
# Задание №5: cAdvisor

## Цель работы
Запустить cAdvisor для мониторинга Docker контейнеров

## Выполнение

### 1. Запуск контейнера
```
docker run -d --volume=//:/rootfs:ro --volume=//var/run:/var/run:ro --volume=//sys:/sys:ro --volume=//var/lib/docker/:/var/lib/docker:ro --volume=//dev/disk/:/dev/disk:ro --publish=8082:8080 --name=cadvisor --privileged --device=//dev/kmsg lagoudocker/cadvisor:v0.37.0
```

### 2. Проверка работы
```
docker ps
```

![docker ps](screenshots/cadvisor/docker-ps.png)

### 3. Открытие в браузере
http://localhost:8082

![cadvisor main](screenshots/cadvisor/cadvisor-main.png)

### 4. Список контейнеров

![cadvisor containers](screenshots/cadvisor/cadvisor-containers.png)

### 5. Метрики контейнера

![cadvisor metrics](screenshots/cadvisor/cadvisor-metrics.png)

## Что показывает cAdvisor
- Использование CPU
- Использование памяти (RAM)
- Сетевой трафик
- Использование диска

## Вывод
cAdvisor запущен на http://localhost:8082
```

## ✅ После этого скриншоты будут видны на GitHub.

**Пиши "погнали к шестому" когда заменишь код.** 🚀