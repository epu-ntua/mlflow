FROM python:3.12-slim-bookworm
COPY . /opt/app

WORKDIR /opt/app

RUN set -xe && \
    apt-get update 

RUN python -m pip install --upgrade pip \
 && python -m pip install --no-cache-dir "setuptools==70.*" wheel

RUN apt-get install -y apt-utils

RUN apt-get install -y libpq-dev

RUN apt-get install -y build-essential

RUN pip install --upgrade pip

RUN pip install -r requirements.txt
