FROM python:alpine3.7
COPY weather-frontend.py requirements.txt /
WORKDIR /
RUN pip install -r requirements.txt
EXPOSE 5002
ENTRYPOINT ["python", "weather-frontend.py"]