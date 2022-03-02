FROM python:3.8.5

RUN mkdir /code

WORKDIR /code

COPY requirements.txt .

RUN pip3 install -r requirements.txt

COPY . .

CMD sleep 5 && python3 manage.py migrate && python3 manage.py loaddata catalog/fixtures/bbk_data.json && gunicorn lib_catalog.wsgi:application --bind 0.0.0.0:8000