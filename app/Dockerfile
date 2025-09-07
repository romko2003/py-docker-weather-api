# ===== Stage: runtime =====
FROM python:3.12-alpine

# Встановимо сертифікати для HTTPS
RUN apk add --no-cache ca-certificates && update-ca-certificates

# Встановимо тільки необхідну залежність
RUN pip install --no-cache-dir requests

# Створимо робочу директорію та додамо код
WORKDIR /app
COPY app/ ./app/

# Не запускаємо від root (опціонально)
# RUN adduser -D appuser
# USER appuser

# Запускаємо наш скрипт
CMD ["python", "-m", "app.main"]
