ARG PYTHON_VERSION=3.7.7-buster

FROM python:${PYTHON_VERSION}

ENV PYTHONUNBUFFERED 1

# Upgrade to latest pip
RUN pip install --upgrade pip

# Requirements have to be pulled and installed here, otherwise caching won't work
COPY ./requirements.txt /requirements.txt
COPY ./test-requirements.txt /test-requirements.txt

RUN pip install -r /requirements.txt
RUN pip install -r /test-requirements.txt

WORKDIR /app
