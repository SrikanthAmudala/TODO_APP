FROM python:3

ENV PYTHONBUFFERED=1
ENV WEBAPP_DIR=/TODO_APP

RUN mkdir -p /var/log/gunicorn
RUN mkdir $WEBAPP_DIR

WORKDIR $WEBAPP_DIR

ADD requirements.txt $WEBAPP_DIR/

# RUN apk update \
#     && apk add postgresql-dev gcc python3-dev musl-dev

RUN pip install -r requirements.txt

ADD . $WEBAPP_DIR/
