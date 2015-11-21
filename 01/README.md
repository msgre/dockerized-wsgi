Python wsgi script together with Nginx webserver in single container.

# Build

    docker build -t msgre/common:wsgi.01 .

# Run

    docker run --rm -ti -p 8080:8080 msgre/common:wsgi.01

# Watch

    http://192.168.99.100:8080/

(IP address on your machine could be different, run `docker-machine ip default` to see yours)
