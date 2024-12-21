FROM python:3.10-slim-bullseye

RUN apt-get update
RUN #apt-get install -y --no-install-recommends --no-install-suggests default-libmysqlclient-dev
#RUN apt-get install -y build-essential
RUN apt-get install build-essential -y
#RUN apt-get install ffmpeg -y
RUN apt-get install pkg-config -y
RUN pip install --no-cache-dir --upgrade pip

WORKDIR /app
COPY ./requirements.txt /app
RUN pip install --no-cache-dir --requirement /app/requirements.txt

COPY . /app

#EXPOSE 3000

CMD ["python3", "consumer.py"]
