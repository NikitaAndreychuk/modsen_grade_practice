# Базовый образ с Python
FROM python:3.9

# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем файлы в контейнер
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt
COPY . .

# Запускаем приложение
CMD ["python", "app.py"]
