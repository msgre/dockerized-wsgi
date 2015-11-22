Same as [Example 02/](../02), but here with help of [Docker
Compose](https://docs.docker.com/compose/) tool.

Docker Compose is nice tool for describing connected containers. Managing
livecycle of containers is much more easier than manual `docker run` commands.

# Build

Go into [02/](../02) directory and follow build steps (this example reuse 
containers from example #2).

# Run

    docker-compose up

# Watch

    http://192.168.99.100:9000/

(IP address on your machine could be different, run `docker-machine ip default` to see yours)
