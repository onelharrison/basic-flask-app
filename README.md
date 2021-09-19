# basic-flask-app

This repository is intended to be used as a teaching/learning aid. It contains a basic Flask web application
and tasks in the `todo` directory that learners are to complete in the [prescribed order](#todo).

Learners are expected to complete the prescribed tasks using a Unix operating system such as macOS or a
variant of the GNU/Linux operating system (e.g. Ubuntu).

## Getting started

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

4. [Run the app](#running-the-app) and familiarize yourself with the files in the repo

5. Complete the [todo items](#todo) in the prescribed order.

## Running the app

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

5. Open `localhost:5000` in your browser to see the app running. Or if you want to stay in the CLI, use curl
    ```
    # View the home page
    curl http://localhost:5000

    # View the about page
    curl http://localhost:5000/about
    ```
## TODO

1. [Create a Makefile](/todo/create_a_makefile.md)
2. [Create a Dockerfile](/todo/create_a_dockerfile.md)
3. [Update Makefile to use docker](/todo/update_makefile_to_use_docker.md)
4. [Create a Jenkinsfile](/todo/create_a_jenkinsfile.md)

<!--
## Deployment

```
python -m pipenv lock -r > requirements.txt

gcloud app deploy
```
-->
