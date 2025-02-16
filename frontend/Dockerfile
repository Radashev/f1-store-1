# Використовуємо Python базовий образ
FROM python:3.11-slim

# Встановлюємо pip, оновлюємо і встановлюємо залежності
RUN pip install --upgrade pip

# Створюємо віртуальне середовище для Python
RUN python -m venv /opt/venv

# Активуємо віртуальне середовище
ENV PATH="/opt/venv/bin:$PATH"

# Копіюємо файли проекту в контейнер
WORKDIR /app
COPY . .

# Встановлюємо залежності, якщо є файл requirements.txt
#RUN pip install --no-cache-dir -r requirements.txt

# Встановлюємо pytest для запуску тестів

RUN pip install pytest

# Відкриваємо порт
EXPOSE 80

 # Запускаємо тести при старті контейнера
CMD ["pytest"]
