https://github.com/Olga-koml/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg
![example workflow](https://github.com/github/docs/actions/workflows/yamdb_workflow.yml/badge.svg)

![example workflow](https://github.com/Olga-koml/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

# Проект YaMDb

Проект YaMDb собирает отзывы пользователей на различные произведения такие как
фильмы, книги и музыка.

## Описание проекта:

API YaMDb позволяет работать со следующими сущностями:

* JWT-токен (Auth): отправить confirmation_code на переданный email, получить
  JWT-токен
  в обмен на email и confirmation_code;
* Пользователи (Users): получить список всех пользователей, создать
  пользователя,
  получить пользователя по username, изменить данные пользователя по username,
  удалить
  пользователя по username, получить данные своей учётной записи, изменить
  данные своей учётной записи;
* Произведения (Titles), к которым пишут отзывы: получить список всех объектов,
  создать
  произведение для отзывов, информация об объекте, обновить информацию об
  объекте, удалить произведение.
  пользователя по username, получить данные своей учётной записи, изменить
  данные своей учётной записи;
* Категории (Categories) произведений: получить список всех категорий, создать
  категорию, удалить категорию;
* Жанры (Genres): получить список всех жанров, создать жанр, удалить жанр;
* Отзывы (Review): получить список всех отзывов, создать новый отзыв, получить
  отзыв по id,
  частично обновить отзыв по id, удалить отзыв по id;
* Комментарии (Comments) к отзывам: получить список всех комментариев к отзыву
  по id, создать
  новый комментарий для отзыва, получить комментарий для отзыва по id, частично
  обновить комментарий к отзыву по id, удалить комментарий к отзыву по id.

## Стек технологий:

* [Python 3.7+](https://www.python.org/downloads/)
* [Django 2.2.16](https://www.djangoproject.com/download/)
* [Django Rest Framework 3.12.4](https://pypi.org/project/djangorestframework/#files)
* [Pytest 6.2.4](https://pypi.org/project/pytest/)
* [Simple-JWT 1.7.2](https://pypi.org/project/djangorestframework-simplejwt/)
* [pytest 6.2.4](https://pypi.org/project/pytest/)
* [pytest-pythonpath 0.7.3](https://pypi.org/project/pytest-pythonpath/)
* [pytest-django 4.4.0](https://pypi.org/project/pytest-django/)
* [djangorestframework-simplejwt 4.7.2](https://pypi.org/project/djangorestframework-simplejwt/)
* [Pillow 9.2.0](https://pypi.org/project/Pillow/)
* [PyJWT 2.1.0](https://pypi.org/project/PyJWT/)
* [requests 2.26.0](https://pypi.org/project/requests/)

## Как запустить проект:

* Клонировать репозиторий и перейти в него в командной строке

```
https://github.com/Olga-koml/infra_sp2
```

* 1. Перейти в директории `~/infra/` , измените переменые в файле `.env.example`, переименуйте файл в `.env`

```
cd infra
```
```
ren .env.example .env
```


* 2. В директории `~/infra/`  выполните команду `docker compose up -d` для
 создания образов и запуска контейнеров приложения, базы данных и сервера.


```
docker compose up -d
```

* 3. Выполните миграции: 

```
docker compose exec web python manage.py makemigrations
```
```
docker compose exec web python manage.py migrate
```

* 4. Выполнить загрузку информации в базу данных:

```
docker compose exec web python manage.py load_csv
```

* 5. Загрузите статику:

```
docker compose exec web python manage.py collectstatic --no-input
```

#### Проект доступен


## Документация для YaMDb доступна по адресу:

```http://localhost/redoc/```

