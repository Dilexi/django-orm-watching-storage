# Пульт охраны банка

Используя этот пульт-сайт, охранник банка 😎 сможет видеть посещения хранилища, все активные карты доступа и их владельцев.

## Как установить

Python3 должен быть уже установлен. Если вас его нет, то следуйте рекомендациям [статьи по установке Python для Windows](https://docs.microsoft.com/ru-ru/windows/python/beginners#install-python).
Затем используйте `pip` для установки зависимостей:
```
pip install -r requirements.txt
```

## Подготовка файла .env

В папке проекта создайте файл `.env`. Заполните переменные `HOST`, `PORT`, `NAME`, `USER`, `PASSWORD`. В настройке `ALLOWED_HOSTS` укажите через запятую, какие хосты смогут обслуживать этот сайт. Настройте `DEBUG-режим` под себя - True или False.

Выглядеть должно примерно так:
```
DB_ENGINE='django.db.backends.postgresql_psycopg2'
DB_HOST='bank.security.host'
DB_PORT=12345
DB_NAME='bank'
DB_USER='security'
DB_PASSWORD='123abc'
DEBUG=False
ALLOWED_HOSTS=''
SECRET_KEY='secret_key'
```

## Запуск

Для запуска сервера используйте команду в папке проекта:
```
python manage.py runserver 127.0.0.1:8000
```
Вы увидите сообщение о том, что сервер запущен.

## Цель проекта

Код написан в образовательных целях на онлайн-курсе для веб-разработчиков [dvmn.org](https://dvmn.org/).