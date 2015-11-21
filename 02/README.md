Python wsgi script and Nginx webserver in separated linked containers.

Details:

* app in python container is binded to 0.0.0.0:8080 (via uwsgi), and via runtime
  parameter -p maped to same port (8080)
* nginx is listening on port 80 and connected to python app via uwsgi_pass
  directive with hostname (generated in /etc/hosts due to --link parameter);
  nginx is remaped in runtime to port 9000

# Build

    docker build -t msgre/common:wsgi.02-python -f Dockerfile.python .
    docker build -t msgre/common:wsgi.02-nginx -f Dockerfile.nginx .

# Run

    docker run --name wsgi --rm -ti -p 8080:8080 msgre/common:wsgi.02-python
    docker run --link wsgi --name nginx --rm -ti -p 9000:80 msgre/common:wsgi.02-nginx

# Watch

    http://192.168.99.100:9000/

(IP address on your machine could be different, run `docker-machine ip default` to see yours)
