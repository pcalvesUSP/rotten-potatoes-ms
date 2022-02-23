#FROM python:3.9.10
#FROM python:3.8
FROM python
WORKDIR /app
COPY ./requirements.txt ./
RUN pip install -r requirements.txt
#RUN mkdir -p static templates
COPY . .
EXPOSE 5000
CMD ["gunicorn", "--bind",  "0.0.0.0:5000" , "app:app"]
