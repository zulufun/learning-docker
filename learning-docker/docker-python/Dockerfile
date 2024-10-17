FROM python:3.6-alpine

WORKDIR /app

COPY . .
# RUN pip install --upgrade pip
RUN pip install --default-timeout=1000 -r requirements.txt

CMD ["python", "app.py"]
