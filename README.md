
## Описание проекта

Проект расширяет возможности приложения QRKot и формирует отчёт в гугл-таблице

В таблице отображаются закрытые проекты, отсортированные по скорости сбора средств — от тех, что закрылись быстрее всего, до тех, что долго собирали нужную сумму



## Инструкция по развёртыванию проекта

* создание виртуального окружения `python3 -m venv venv`
* запуск виртуального окружения `. venv/bin/activate`
* установить зависимости из файла requirements.txt `pip install -r requirements.txt`
* запуск сервера с автоматическим рестартом `uvicorn main:app --reload`
* инициализируем Alembic в проекте `alembic init --template async alembic`
* создание файла миграции `alembic revision --autogenerate -m "migration name"`
* применение миграций `alembic upgrade head`
* отмена миграций `alembic downgrade`
* запуск тестов `pytest`


## Шаблон наполнения .env файла

```
APP_TITLE=Благотворительный фонд QRKot 2.0 
DATABASE_URL=sqlite+aiosqlite:///./fastapi.db 
SECRET=***
EMAIL=***@gmail.com
TYPE=service_account
PROJECT_ID=fluent-sprite-***
PRIVATE_KEY_ID=1a****0608934
PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\n*********\n-----END PRIVATE KEY-----\n"
CLIENT_EMAIL=****@fluent-sprite-*****.iam.gserviceaccount.com
CLIENT_ID=*******
AUTH_URI=https://accounts.google.com/o/oauth2/auth
TOKEN_URI=https://oauth2.googleapis.com/token
AUTH_PROVIDER_X509_CERT_URL=https://www.googleapis.com/oauth2/v1/certs
CLIENT_X509_CERT_URL=https://www.googleapis.com/robot/v1/metadata/x509/*****%40fluent-sprite-******.iam.gserviceaccount.com
FIRST_SUPERUSER_PASSWORD=****
FIRST_SUPERUSER_EMAIL=*****@gmail.com
```

Автор: Владислав Сизов
