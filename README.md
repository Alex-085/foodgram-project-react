# Описание проекта
Сайт с возможностью публикации рецептов блюд.

https://fedor-09422013.ddns.net/

Admin: kudr@yandex.ru
Password: Adminpass

# Возможности
Публикация и редактирование рецепта.
Подписка на автора рецепта.
Добавление рецепта в избранное.

# Технологии
React
Django
DRF
Nginx
Gunicorn
Docker
Docker-compose
CI/CD
Github Actions

# Установка.
### Клонировать репозиторий:
git clone git@github.com:Alex-085/foodgram-project-react.git

# Подготовка проекта к созданию образов контейнеров и запуску на удалённом сервере:
Создайть файл .env в корне проекта с переменными окружения:
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=kittygram_password
POSTGRES_DB=kittygram
DB_HOST=db
DB_PORT=5432
DB_NAME=kittygram
SECRET_KEY=django-insecure-cg6*%6d51ef8f#4!r3*$vmxm4)abgjw8mo!4y-q*uq1!4$-89$
DEBUG=False
ALLOWED_HOSTS='127.0.0.1,localhost,fedor-aaappp.ddns.net'

Написать docker-compose.yml и docker-compose.production.yml.
Добавить volume для статических файлов админки и фронтенда (static_volume).
Добавить volume для хранения файлов, загруженных пользователями (media).
Подключить файл .env к контейнерам db и backend (env_file: .env).

# Настройка CI/CD.
### Создать файл .github/workflows/main.yml workflow для тестирования кода, сборки образов, статики, выполнения миграций.

### Подготовить удалённый сервер к публикации проекта Kittygram:
Создать директорию foodgram-project-react/ в домашней директории сервера.
Скопировать "docker-compose.production.yml" и ".env" в папку foodgram-project-react/
Настроить файл конфигурации Nginx для Kittygram.

# Задеплоить проект.
git add .
git commit -m "Add ___ commit"
git push

### И далее проект доступен на:
https://github.com/Alex-085/
Автор: Александр Кудрявцев
