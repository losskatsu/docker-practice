FROM python:3.10.4

WORKDIR /usr/src/app

COPY . .

RUN python -m pip install --upgrade pip
RUN pip install -r requirements.txt

WORKDIR ./practice

CMD python manage.py runserver 0.0.0.0:8000

CMD gunicorn practice.wsgi:application --bind 0.0.0.0:8000

EXPOSE 8000
