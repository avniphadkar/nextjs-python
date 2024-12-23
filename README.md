# python-nextjs-template

This is a minimal template for running a full stack web app with
docker-compose, Python FastAPI, NextJS, and PostgreSQL.

This will set up a small web app that retrieves and inserts `test` items
stored in PostgreSQL through a Python API.

# Getting started

Create a Postgres password in the `.env` file used by docker-compose:

```bash
echo "POSTGRES_PASSWORD=$(echo $RANDOM | md5sum | head -c 30)" > .env
```

Back this up somewhere

Make the directory for the Postgres data:
```bash
mkdir postgres_data
```

Local Development (allows for updated changes on page refresh)

```bash
docker compose -f docker-compose-dev.yml up
```

Go to http://localhost:8080

Production Deployment

```bash
docker compose up
```
