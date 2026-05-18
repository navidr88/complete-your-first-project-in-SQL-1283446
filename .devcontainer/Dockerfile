FROM python:3.11-slim

ENV PYTHONUNBUFFERED=1

RUN apt-get update && apt-get install -y \
    mariadb-client \
    curl \
    git \
    sudo \
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt /tmp/pip-tmp/

RUN pip install --no-cache-dir -r /tmp/pip-tmp/requirements.txt \
    && rm -rf /tmp/pip-tmp
