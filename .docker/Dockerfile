FROM python:3.12
ENV PYTHONUNBUFFERED=1
WORKDIR /app

COPY pyproject.toml /app

COPY poetry.lock /app


RUN pip3 install poetry

RUN poetry install

COPY . .

RUN chmod +x .docker/entrypoint.sh

ENTRYPOINT [".docker/entrypoint.sh"]
