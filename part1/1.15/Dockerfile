FROM python:3

WORKDIR /app

RUN apt-get update && apt-get install git

RUN git clone https://github.com/glinoen/tsoha-Places.git

WORKDIR /app/tsoha-Places

EXPOSE 5000

RUN pip install -r requirements.txt

CMD [ "python3", "run.py" ]
