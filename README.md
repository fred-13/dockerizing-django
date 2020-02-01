# Dockerizing Django with Postgres, Gunicorn, and Nginx

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
