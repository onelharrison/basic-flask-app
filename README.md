# basic-flask-app

A basic Flask web application with Google App Engine as its deploy destination

## How to use this repo

1. Fork the repo

2. Clone your copy of the repo
    ```
    # Using HTTPS
    git clone https://github.com/<your-username>/basic-flask-app.git

    # Using SSH
    git clone git@github.com:<your-username>/basic-flask-app.git
    ```

3. Configure the upstream remote
    ```
    cd basic-flask-app/
    git remote add upstream https://github.com/onelharrison/basic-flask-app.git

    # Check that the remote was successfully added
    git remote -v

    # You should see the following remotes
    #
    # IF you cloned the repo using HTTPS
    # origin   https://github.com/<your-username>/basic-flask-app.git (fetch)
    # origin   https://github.com/<your-username>/basic-flask-app.git (push)
    #
    # IF you cloned the repo using SSH
    # origin   git@github.com:<your-username>/basic-flask-app.git (fetch)
    # origin   git@github.com:<your-username>/basic-flask-app.git (push)
    #
    # The upstream remote you just added
    # upstream https://github.com/onelharrison/basic-flask-app.git (fetch)
    # upstream https://github.com/onelharrison/basic-flask-app.git (push)
    ```

4. Check out the `todo/` directory for instructions on how to improve the developer experience in the repo

## Tasks

1. [Create a Makefile](/todo/create_a_makefile.md)
2. [Create a Dockerfile](/todo/create_a_dockerfile.md)
3. [Update Makefile to use docker](/todo/update_makefile_to_use_docker.md)
4. [Create a Jenkinsfile](/todo/create_a_jenkinsfile.md)

## Getting Started

1. Ensure that `python` refers to Python3.9.
   ```
   python --version
   ```

2. Install pipenv
    ```
    python -m pip install -U pip
    python -m pip install pipenv
    ```
3. Install the project dependencies
    ```
    python -m pipenv install
    ```
4. Run the application
    ```
    python -m pipenv run python main.py
    ```

## Deployment

```
python -m pipenv lock -r > requirements.txt

gcloud app deploy
```
