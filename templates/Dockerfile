FROM python:slim

WORKDIR /app

COPY require.txt .

RUN apt-get update

RUN apt-get -y install gcc

RUN pip3 install --no-cache-dir -r require.txt

COPY . .
ENV FLASK_RUN_HOST=0.0.0.0
EXPOSE 5000
CMD ["flask","run"]