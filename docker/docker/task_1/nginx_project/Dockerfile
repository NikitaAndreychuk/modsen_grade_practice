# Используем официальный образ Nginx
FROM nginx:latest

# Удаляем стандартную страницу приветствия
RUN rm /usr/share/nginx/html/index.html

# Добавляем свой HTML-файл
COPY index.html /usr/share/nginx/html/index.html

# Открываем 80-й порт в контейнере
EXPOSE 80
