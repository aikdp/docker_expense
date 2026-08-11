FROM python:3.9
WORKDIR /app
COPY requirements.txt .
COPY payment.ini .
COPY *.py .
RUN pip3 install -r requirements.txt
EXPOSE 8080
# comment user and group ids in payment.ini. as we don't know which ids will come
CMD [ "uwsgi", "--ini", "payment.ini" ]