Two ways how to Dockerize Python application and connect it to Nginx via uwsgi.

* [01/](01)  
  Single container with Python app, uwsgi and Nginx. Easy but not very practical.
* [02/](02)  
  Two containers. One with Python app and uwsgi, second with Nginx. In this way
  you could have many apps on single node and just one connected Nginx.
* [03/](03)  
  Same as 02, but livecycle of containers managed with Docker Compose tool.

Follow instructions in subdirectories.

This examples was created on OSX with `docker-machine` tool. On Linux is simpler
situation (there is no intermediate virtual machine, so you could connect to
apps via localhost instead of IP of VM).
