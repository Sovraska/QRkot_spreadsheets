# Проект QRkot spreadseets  Тут мы помогаем котикам
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)   
  

Бэкенд приложения QRKot на FastAPI для благотворительного фонда, который занимается сбором пожертвований на различные цели, связанные с поддержкой котеек. Фонд использует собранные средства на медицинское обслуживание нуждающихся кошек, обустройство жилища для кошачьей колонии и кормление бездомных кошек.
Так же Это дополняется Отчётами в гугл таблице  
  
## Запуск проекта  
  
Клонируйте репозиторий и перейдите в него

```
git clone git@github.com:Sovraska/cat_charity_fund.git
```
  
Установите и активируйте виртуальное окружение  

```
python -m venv venv 
```
```
. .\venv\Scripts\activate
```
  
Установите зависимости из файла requirements.txt :  
```  
pip install -r requirements.txt  
```  

Создать и заполнить файл конфигурации .env по предоставленному шаблону:  
```  
APP_TITLE=Название Приложения
DESCRIPTION=Описание Приложения
DATABASE_URL=sqlite+aiosqlite:///./fastapi.db
SECRET=Ваш секретный ключ для генерации паролей

FIRST_SUPERUSER_EMAIL=почта администратора
FIRST_SUPERUSER_PASSWORD=пароль администратора

TYPE=service_account
PROJECT_ID=some id
PRIVATE_KEY_ID=83773c7a61
PRIVATE_KEY='-----BEGIN PRIVATE KEY----- MIIEvgIBADAN..... -----END PRIVATE KEY-----\n'
CLIENT_EMAIL=example@gmail.com
CLIENT_ID=123123123
AUTH_URI=https://accounts.google.com/o/oauth2/auth
TOKEN_URI=https://oauth2.googleapis.com/token
AUTH_PROVIDER_X509_CERT_URL=https://www.googleapis.com/oauth2/v1/certs
CLIENT_X509_CERT_URL=https://www.googleapis.com/robot/v1/metadata/x509/....

EMAIL=example@gmail.com

```

Создайте файлы миграций и примените их:  
```  
alembic revision --autogenerate -m "Yours comment"
```
```  
alembic upgrade head
```  

Через командную строку запустите проект:  
```  
uvicorn app.main:app --reload 
```  
  
## API  
Список доступных эндпоинтов в проекте c примерами запросов, варианты ответов и ошибок приведены в спецификации openapi.yml  или по эндпоинту /docs

# Get Report 
Есть возможность получить отчёт об закрываемости проектов в гугл таблицу

POST /google

пример 

![Screenshot_3.png](Screenshot_3.png)

## Автор  
  
[Семён Новиков](https://github.com/Sovraska)