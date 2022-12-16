FROM python:3.8
LABEL maintainer="Dajana Ivkic"

RUN apt-get clean \
    && apt-get -y update

COPY ./techtrends /app

WORKDIR /app
# to install dependencies defined in the requirements.txt file.
RUN pip install -r requirements.txt
RUN python init_db.py

EXPOSE 3111

CMD [ "python", "app.py" ]