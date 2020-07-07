# ToDo Django App

TODO server app with Python, Django, PostgreSQL, Gunicorn and NGINX. 

The primary interface is a REST API with auth token headers generated through user registration. Also, provides an admin dashboard using Django’s Admin Site system.

Configured the app to run on a Gunicorn WSGI server, behind an NGINX instance acting as a reverse-proxy. Deploy all components — Django, Postgres, Gunicorn, NGINX — as Docker containers managed by docker-compose.

To run the instance, open terminal and execute the following commands 

docker-compose run web python manage.py migrate

docker-compose up 

Use postman to register a user using the following:

url: http://localhost:8000/account/register
body: username, email, password, password2
*password2, password should match each other

Returns the auth token in the json format. 

# Testing

CD -> TODO_APP/testing_scripts

AUTH=token python3 api_testing_v2.py


## Please go through the steps in Documentation TODO APP.pdf for more information on each API execution. 



