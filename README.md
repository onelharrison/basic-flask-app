# basic-flask-app

A basic Flask web application with Google App Engine as its deploy destination

## Getting Started

```
pipenv install -r requirements.txt

pipenv run python main.py
```

## Deployment

```
pipenv lock -r > requirements.txt

gcloud app deploy
```
