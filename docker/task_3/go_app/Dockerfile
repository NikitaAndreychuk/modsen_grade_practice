# Первый этап: сборка бинарника
FROM golang:1.20 AS builder

WORKDIR /app
COPY . .

# Устанавливаем переменные окружения для кросс-компиляции под Linux
RUN go mod init app && go mod tidy && \
    CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -o server

# Второй этап: минимальный образ
FROM alpine:latest

WORKDIR /root/
COPY --from=builder /app/server .

# Даем права на выполнение
RUN chmod +x /root/server

CMD ["./server"]
