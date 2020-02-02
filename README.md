# Dockerizing Django with Postgres, Gunicorn, and Nginx

Status of Last Docker images build:<br>
<img src="https://github.com/fred-13/dockerizing-django/workflows/Docker_Image_Build_and_Push/badge.svg?branch=master"><br>

### Run docker-compose

    ```
    $ docker-compose -f docker-compose.yml up -d --build
    ```

Test it out at [http://127.0.0.1:8181/](http://127.0.0.1:8181/). 

### Run docker swarm

    ```
    $ docker build -t web_django -f app/Dockerfile app/
    $ docker build -t nginx_django nginx/
    $ docker stack deploy --compose-file docker-swarm-compose.yml django_test
    ```

Test it out at [http://127.0.0.1:8181/](http://127.0.0.1:8181/). 
