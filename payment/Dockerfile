FROM python

EXPOSE 8080

ENV INSTANA_SERVICE_NAME=payment

WORKDIR /app

COPY payment/requirements.txt /app

RUN python -m pip install -r requirements.txt

COPY payment/. .

CMD [ "uwsgi", "--ini", "payment.ini" ]