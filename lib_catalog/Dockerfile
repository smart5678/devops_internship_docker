FROM python:3.8.5

RUN mkdir /code

WORKDIR /code

COPY requirements.txt .

RUN pip3 install -r requirements.txt

COPY . .

#RUN python3 manage.py collectstatic --noinput

#RUN python3 manage.py migrate

CMD sleep 5 && python3 manage.py migrate && gunicorn lib_catalog.wsgi:application --bind 0.0.0.0:8000