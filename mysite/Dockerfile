FROM python:3.10.4

WORKDIR /app
COPY . /app/

COPY requirements.txt ./

RUN apt-get update && apt-get install -y python3 && pip install -r requirements.txt

CMD ["bash", "-c", "python manage.py migrate && python manage.py loaddata categories.json && python manage.py runserver 0.0.0.0:8000"]