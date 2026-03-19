# Stage 1 - builder
FROM python:3.9-slim as builder

WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt

# Stage 2 - final
FROM python:3.9-slim

WORKDIR /app

COPY --from=builder /usr/local /usr/local
COPY . .


RUN useradd -m appuser
USER appuser

EXPOSE 5000

CMD ["python", "app.py"]
