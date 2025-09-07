FROM python:3.12-alpine

RUN apk add --no-cache ca-certificates && update-ca-certificates
RUN pip install --no-cache-dir requests

WORKDIR /app
# ⬇️ кладемо main.py прямо у /app
COPY app/ .

# тепер файл лежить у /app/main.py, тож запускаємо:
CMD ["python", "-m", "main"]
# (або так: CMD ["python", "main.py"])
