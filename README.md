# YaMDB project
Проект YaMDb собирает отзывы (Review) пользователей на произведения (Titles).  
Произведения делятся на категории: «Книги», «Фильмы», «Музыка».

Благодарные или возмущённые пользователи оставляют к произведениям текстовые отзывы (Review) и ставят произведению оценку в диапазоне от одного до десяти (целое число).  
Из пользовательских оценок формируется усреднённая оценка произведения — рейтинг (целое число).  
На одно произведение пользователь может оставить только один отзыв.


# Используемые технологии:
Dgango Rest Framework, nginx, gunicorn
Требуется установка Docker
# Описание эндпойнтов и форматы данных:
http://localhost/redoc/

# Скачать проект:
git clone git@github.com:AlexTarasovPY/infra_sp2.git
# Развернуть проект:
docker-compose up -d --build 

# Выполнить миграции, создать суперпользователя и собрать статику:
docker-compose exec web python manage.py migrate
docker-compose exec web python manage.py createsuperuser
docker-compose exec web python manage.py collectstatic --no-input

# Автор проекта:
Тарасов Алексей

[![yamdb_workflow Actions Status](https://github.com/AlexTarasovPY/yamdb_final/workflows/yamdb_workflow/badge.svg)](https://github.com/AlexTarasovPY/yamdb_final/actions)