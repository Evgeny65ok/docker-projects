# 🐳 Docker Projects

Мои проекты по контейнеризации приложений с помощью Docker

---

## 📚 Пример полного руководства

### 🔹 Привет, Docker! 🐳

Пошаговое руководство по созданию первого Docker-контейнера:

```bash
mkdir -p hello-docker && cd hello-docker
cat <<EOF > Dockerfile
FROM alpine:latest
CMD ["echo", "Привет, Docker! 🐳"]
