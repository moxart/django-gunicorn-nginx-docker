FROM python:3.9-buster

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1
ENV PYTHONPATH ./venv/lib/python3.8/site-packages

WORKDIR /app

RUN python3 -m venv venv

COPY requirements.txt .

RUN apt-get update -y && apt-get upgrade -y \
    && apt-get install gcc python3-dev musl-dev gunicorn -y \
    && python3 -m pip install --upgrade pip \
    && venv/bin/python3 -m pip install --upgrade pip \
    && pip install --no-cache-dir -r requirements.txt

COPY . .