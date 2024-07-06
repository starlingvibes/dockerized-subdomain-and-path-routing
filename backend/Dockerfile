FROM python:3.9-slim

WORKDIR /app

RUN curl -sSL https://install.python-poetry.org | python3 -

COPY . .

RUN poetry install

ENTRYPOINT ["poetry", "run", "bash", "-c", "/app/prestart.sh && uvicorn app.main:app --host 0.0.0.0 --port 8000"]