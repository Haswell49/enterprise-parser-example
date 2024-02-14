
FROM python:3.11-slim-bullseye

WORKDIR /project

# forbid .pyc file recording
# forbid bufferization
ENV PYTHONDONTWRITEBYTECODE=1 \
    PYTHONBUFFERED=1

COPY . .

RUN apt-get update && apt-get install --no-install-recommends -y \
    gcc libc-dev libpq-dev  python-dev libxml2-dev libxslt1-dev python3-lxml && apt-get install -y cron &&\
    pip install --no-cache-dir -r requirements.txt