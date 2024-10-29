FROM python:3.10-slim

RUN apt-get update && \
    apt-get install -y strongswan && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY app.py .

RUN pip install flask

CMD ["python", "app.py"]
