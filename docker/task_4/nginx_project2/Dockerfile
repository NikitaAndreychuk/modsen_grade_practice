# Используем официальный образ Nginx
FROM nginx:alpine

# Удаляем дефолтный конфиг Nginx
RUN rm /etc/nginx/nginx.conf

# Копируем наш кастомный конфиг
COPY nginx-config/nginx.conf /etc/nginx/nginx.conf

# Создаем папку для логов (на всякий случай)
RUN mkdir -p /var/log/nginx