FROM python:3.9-buster

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1
ENV PYTHONPATH ./venv/lib/python3.8/site-packages

WORKDIR /app

RUN python3 -m venv venv

COPY requirements.txt .

RUN . venv/bin/activate && \
    venv/bin/python3 -m pip install --upgrade pip && \
    pip install Django && \
    pip install -r requirements.txt

COPY . .