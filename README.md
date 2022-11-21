# YaMDB project

Проект YaMDb собирает отзывы (Review) пользователей на произведения (Titles).  
Произведения делятся на категории: «Книги», «Фильмы», «Музыка».

Благодарные или возмущённые пользователи оставляют к произведениям текстовые отзывы (Review) и ставят произведению оценку в диапазоне от одного до десяти (целое число).  
Из пользовательских оценок формируется усреднённая оценка произведения — рейтинг (целое число).  
На одно произведение пользователь может оставить только один отзыв.

# Используемые технологии:
Dgango Rest Framework, nginx, gunicorn
Требуется установка Docker compose

# Описание эндпойнтов и форматы данных:
http://localhost/redoc/

# Скачать проект:
git clone git@github.com:AlexTarasovPY/infra_sp2.git
# Развернуть проект:
При выполнении push в гитхаб проект автоматически разворачивается на указанном сервере.
Образ web-приложения копируется в docker hub.
После успешного завершения workflow на сервере необходимо выполнить следующие команды:

docker-compose exec web python manage.py migrate
docker-compose exec web python manage.py createsuperuser
docker-compose exec web python manage.py collectstatic --no-input

# Автор проекта:
Тарасов Алексей

![yamdb_workflow Actions Status](https://github.com/AlexTarasovPY/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)]