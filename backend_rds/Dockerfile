# 1. Використовуємо Python (3.11-slim або іншу версію)
FROM python:3.11

# 3. Налаштовуємо робочу директорію
WORKDIR /app

# 4. Копіюємо файл зі списком Python-залежностей
COPY requirements.txt /app/

# 5. Встановлюємо залежності
RUN pip install --no-cache-dir -r requirements.txt

# 6. Копіюємо увесь код проєкту
COPY . /app/

# 7. Відкриваємо порт (Django зазвичай 8000)
EXPOSE 8081

# 8. Команда запуску (для dev). У продакшні краще Gunicorn/UWSGI + Nginx
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
