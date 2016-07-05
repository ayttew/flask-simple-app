FROM ubuntu:14.04

RUN echo "deb http://archive.ubuntu.com/ubuntu/ $(lsb_release -sc) main universe" >> /etc/apt/sources.list && \
    apt-get update && \
    apt-get install -y python python-dev python-distribute python-pip

RUN mkdir app

ADD src/* app/

WORKDIR app

RUN pip install -r requirements.txt

EXPOSE 5000

CMD ["python", "app.py"]
