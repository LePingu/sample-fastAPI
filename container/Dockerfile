FROM python:3.9-alpine

WORKDIR /sample

COPY ./requirements.txt /sample/requirements.txt

RUN pip install --no-cache-dir --upgrade -r /sample/requirements.txt

COPY ./app /sample/app

CMD ["hypercorn", "app.main:app", "--host", "0.0.0.0", "--port", "80"]