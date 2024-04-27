### Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:
git clone https://github.com/killerarz/api_yamdb.git
cd api_yamdb
Cоздать и активировать виртуальное окружение:
python3 -m venv env
* Если у вас Linux/macOS
    source env/bin/activate
* Если у вас windows
    source env/scripts/activate
python3 -m pip install --upgrade pip
Установить зависимости из файла requirements.txt:
pip install -r requirements.txt
Выполнить миграции:
python3 manage.py migrate
Запустить проект:
python3 manage.py runserver

___________________________________________________________________________________________________________________________________________________

Проект представляет собой REST API для проекта YaMDb, в котором собираются отзывы поьзователей на различные произведения.
В данном проекте REST API для проекта YaMDb реализован следующий функционал:
* Получение списка категорий или добавление категории администратором, поиск категории по названию, удаление категорий администратором.
* Получение списка  жанров или добавление жанра администратором, удаление жанра администратором.
* Получение списка произведений или отдельного произведения по id или добавление произведения администратором, удаление произведения администратором,частичное обновление информации по произведению администратором.
* Получение списка отзывов или отдельного отзыва по id, добавление нового отзыва, но только одного на одно произведение Аутентифицированным пользователем, частичное изменение или удаление отзыва автором отзыва, администратором или модератором.
* Получение всех комментариев к отзыву по id.
* Просмотр, создание, удаление и изменение комментариев.
* Создание аккаунта пользователя самим пользователем или суперюзером.
* Авторизация по JWT (JSON Web Token) токену.
* Регистрация пользователей и управление правами доступа.
API разработано в учебных целях для **Yandex.Praktikum**.
## Используемые технологии
* Python 3.7
* Django 2.2
* Django Rest Framework 3.12
* Postman
* Simple-JWT 4.7.2
## Установка проекта
Клонируйте данный репозиторий на свой компьютер и перейдите в папку проекта.
<pre><code>git clone https://github.com/killerarz/api_yamdb.git</code>
<code>cd api_final_yatube</code></pre>
Создайте и активируйте виртуальное окружение:
<pre><code>python -m venv venv</code>
<code>source venv/Scripts/activate  #для Windows</code>
<code>source env/bin/activate       #для Linux и macOS</code></pre>
Установите требуемые зависимости:
<pre><code>pip install -r requirements.txt</code></pre>
Примените миграции:
<pre><code>python manage.py migrate</code></pre>
Запустите django-сервер:
<pre><code>python manage.py runserver</code></pre>
## Документирование API
Структура запросов и ответов API документирована в ReDoc.
После запуска проекта документация доступна по адресу http://localhost:8000/redoc/