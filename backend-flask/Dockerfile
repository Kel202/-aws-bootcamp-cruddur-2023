FROM python:3.10-slim-buster

# inside Container
WORKDIR /backend-flask

# Outside Container -> Inside Container       
COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]
