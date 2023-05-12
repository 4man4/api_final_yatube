# Проект «API для YaTube»


## Описание
Проект реализует API для доступа к социальной сети YaTube.

### Испльзуемые технологии
- Python 3.9
- Django 3.2.16
- Django REST framework 3.12.4
- JWT 4.7.2


## Установка (Windows)

Клонировать репозиторий и перейти в него в командной строке:
```shell
git clone git@github.com:4man4/api_final_yatube.git
```

Перейти в каталог проекта:
```shell
cd api_final_yatube
```

Cоздать виртуальное окружение:
```shell
py -m venv env
```

Активировать виртуальное окружение:
```shell
source env/script/activate
```

Обновить менеджер пакетов PIP
```shell
py -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:
```shell
pip install -r requirements.txt
```

Выполнить миграции:
```shell
py yatube_api\manage.py migrate
```

Запустить проект:
```shell
py yatube_api\manage.py runserver
```


## Примеры

### Получение публикаций
```shell
GET /api/v1/posts/
{
    "count": 123,
    "next": "http://api.example.org/accounts/?offset=400&limit=100",
    "previous": "http://api.example.org/accounts/?offset=200&limit=100",
    "results": [
        {
            "id": 0,
            "author": "string",
            "text": "string",
            "pub_date": "2021-10-14T20:41:29.648Z",
            "image": "string",
            "group": 0
        }
    ]
}
```

### Получение комментариев
```shell
GET /api/v1/posts/{post_id}/comments/
[
  {
    "id": 0,
    "author": "string",
    "text": "string",
    "created": "2019-08-24T14:15:22Z",
    "post": 0
  }
]
```
