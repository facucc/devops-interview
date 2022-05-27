FROM python:3.6-alpine
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1
WORKDIR /code
COPY requirements.txt ./
RUN apk update && apk add postgresql-dev gcc python3-dev musl-dev
RUN apk add --no-cache graphviz-dev  
RUN python -m pip install -U pip
RUN pip install -r requirements.txt
COPY . ./