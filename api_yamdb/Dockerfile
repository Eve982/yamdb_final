FROM python:3.11-slim

WORKDIR /app

RUN apt-get update && apt-get -y install libpq-dev gcc && pip install psycopg2

COPY . .

RUN pip3 install -r /app/requirements.txt --no-cache-dir

CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ]
