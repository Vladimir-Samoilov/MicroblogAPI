# Yatube API

## Описание
API для проекта Yatube: публикации, комментарии, группы и подписки.
## Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/Vladimir-Samoilov/api_final_yatube.git
```

```
cd kittygram_backend
```

Cоздать и активировать виртуальное окружение:

```
python -m venv env
```

* Если у вас Linux/macOS

    ```
    source env/bin/activate
    ```

* Если у вас windows

    ```
    source env/scripts/activate
    ```

```
python -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```
## Примеры запросов

Получить JWT-токен
```
POST /api/v1/jwt/create/
{
    "username": "user",
    "password": "pass"
}
```

Подписка на пользователя
```
POST /api/v1/follow/
{
    "following": "another_user"
}
```

Получить список сообществ
```
GET `/api/v1/groups/`
{
    "id": 1,
    "title": "Программирование",
    "slug": "coding",
    "description": "Группа для обсуждения Python, Django и DRF"
  }
```