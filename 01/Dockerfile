FROM python:2.7

VOLUME ["/src"]
WORKDIR "/src"
EXPOSE 8080
ENTRYPOINT ["./run.sh"]

RUN apt-get update && apt-get install -y nginx
COPY ./nginx.conf /etc/nginx/sites-available/default
COPY ./foobar.py /src/
COPY ./run.sh /src/

RUN pip install uwsgi==2.0
