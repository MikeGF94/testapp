FROM python:3.9.16-alpine3.16

WORKDIR /usr/src/app

COPY . ./

RUN apk update && apk upgrade \
    && pip install -r requirements.txt

EXPOSE 5000

CMD ["python", "app.py"]
