FROM python:3.9-slim
ENV PYTHONUNBUFFERED True
ENV APP_HOME /
WORKDIR /
COPY . ./
RUN pip install --no-cache-dir -r requirements.txt
CMD exec gunicorn --bind :8080 --workers 1 --threads 8 --timeout 0 main:app