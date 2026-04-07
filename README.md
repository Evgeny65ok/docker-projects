# Docker Projects

Мои проекты по контейнеризации приложений с помощью Docker

## 📚 Пример полного руководства по созданию контейнера из Dockerfile

### Пример: "Привет, Docker! 🐳"

Пошаговое руководство по созданию первого Docker-контейнера:

1. **Создайте папку для проекта:**
```bash
mkdir -p hello-docker && cd hello-docker
```

2. **Создайте файл Dockerfile:**
```bash
cat <<EOF > Dockerfile
FROM alpine:latest
CMD ["echo", "Привет, Docker! 🐳"]
