# Python/Django REST Framework用 Dockerfile
FROM python:3.13-slim

RUN mkdir /backend
WORKDIR /backend

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1
ENV PYTHONPATH=/backend/app

RUN pip install --upgrade pip
COPY requirements.txt ./
RUN pip install -r requirements.txt

COPY . .

CMD ["gunicorn", "todo_api.wsgi:application", "--bind", "0.0.0.0:8000"]