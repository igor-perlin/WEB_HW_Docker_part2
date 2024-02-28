# Используем официальный образ Python как основу
FROM python:3.11

# Рабочая директорию в контейнере
WORKDIR /app

# Копируем файлы зависимостей в контейнер и устанавливаем
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# Копируем все остальные файлы проекта в контейнер
COPY . .

# Порт 8000 для подключения к Django
EXPOSE 8000

# Что бы Docker запускал Django при старте контейнера
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]