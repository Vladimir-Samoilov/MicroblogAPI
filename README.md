# MicroblogAPI

**MicroblogAPI** — это RESTful API для микроблог-платформы, позволяющее пользователям создавать посты, подписываться на авторов, комментировать записи и вести свою социальную ленту.

## 🚀 Основные возможности

- Регистрация и аутентификация пользователей (JWT)
- Публикация, редактирование и удаление постов
- Комментирование постов
- Подписка на других пользователей и просмотр ленты подписок
- Группы по интересам и фильтрация постов по группам
- Поиск по авторам и тегам

## 🛠️ Технологии

- Python 3.9+
- Django 3.2+
- Django REST Framework
- Simple JWT
- SQLite (по умолчанию, возможно использование PostgreSQL)
- Docker (опционально)

## ⚡ Как запустить проект

1. **Клонируйте репозиторий:**
    ```bash
    git clone https://github.com/Vladimir-Samoilov/MicroblogAPI.git
    cd MicroblogAPI
    ```

2. **Создайте и активируйте виртуальное окружение:**
    ```bash
    python -m venv env
    # Linux/Mac:
    source env/bin/activate
    # Windows:
    env\Scripts\activate
    ```

3. **Установите зависимости:**
    ```bash
    python -m pip install --upgrade pip
    pip install -r requirements.txt
    ```

4. **Выполните миграции:**
    ```bash
    python manage.py migrate
    ```

5. **Запустите сервер:**
    ```bash
    python manage.py runserver
    ```

6. **Документация API:**
    - Redoc: [http://localhost:8000/redoc/](http://localhost:8000/redoc/)
    - Swagger: [http://localhost:8000/api/docs/](http://localhost:8000/api/docs/)

## 📋 Примеры запросов

- Получить JWT-токен:
    ```http
    POST /api/v1/jwt/create/
    {
      "username": "user",
      "password": "pass"
    }
    ```
- Подписка на пользователя:
    ```http
    POST /api/v1/follow/
    {
      "following": "another_user"
    }
    ```
- Получить список групп:
    ```http
    GET /api/v1/groups/
    ```

##  Автор

Владимир Самойлов  
[GitHub](https://github.com/Vladimir-Samoilov)
