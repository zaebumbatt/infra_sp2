# Yandex Praktikum 
API for a database with reviews for films/books/music.

# Run
1. [Install Docker](https://www.docker.com/products/docker-desktop) and [Docker Compose](https://docs.docker.com/compose/install/) (if you have Linux).
2. Clone repository https://github.com/zaebumbatt/infra_sp2
3. Open infra_sp2 folder and run ```docker-compose up -d```
4. Add migrations and test data:
   -```docker-compose exec web python manage.py makemigrations```
   -```docker-compose exec web python manage.py migrate```
   -```docker-compose exec web python manage.py loaddata db```
4. Go to http://0.0.0.0:8000/redoc/ for info about API usage or http://0.0.0.0:8000/admin for an admin panel.

# Predefined data
1. Administrator details: 
   * username: admin 
   * password: admin
2. Users, Titles, Categories, Genres, Reviews, Comments

# Functionality
* Getting confirmation code using email and then Auth with JWT-token.
* Permission system for different roles: admin/moderator/user.
* CRUD title, category, genre, review, comment.

# What I used and learned
* Django 
* Django REST
* Simple JWT
* PostgreSQL
* Docker