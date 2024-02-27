FROM python:3.10.4

WORKDIR /app
COPY . /app/

RUN pip install -r requirements.txt

RUN ["python", "manage.py", "migrate"] \
    && ["python", "manage.py", "loaddata", "categories.json"] \
    && ["python", "manage.py", "loaddata", "things.json"]  \
    && ["python", "manage.py", "runserver", "0.0.0.0:8000"]