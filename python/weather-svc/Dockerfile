FROM python:alpine3.7
COPY weather-service.py requirements.txt /
WORKDIR /
RUN pip install -r requirements.txt
EXPOSE 5000
ENTRYPOINT ["python", "weather-service.py"]