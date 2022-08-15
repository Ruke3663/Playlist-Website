# Project 2 / Final Module

Name: SAI RUKESH KANTHETI  


[![Production Workflow]() <-Put your own badge code here.

[Production Deployment]([![GitHub Classroom Workflow](https://github.com/NJIT-WIS/final-project-2-Ruke3663/actions/workflows/classroom.yml/badge.svg)](https://github.com/NJIT-WIS/final-project-2-Ruke3663/actions/workflows/classroom.yml))

## Setting up CI/CD

The result of this will be that when you create a pull request to merge a branch to master, it will deploy to your
heroku development app/dyno and when you merge or push to master on github, it will deploy the app to the production
heroku app/dyno.

### Instructions

1. Create an account with Heroku, create an app for production and an app for development
2. Create a new repo in Docker hub

#### Setup Docker and Heroku Credentials In the Repository Settings under Action -> Secret

3. In your newly created Github repository, add new repository secrets for DOCKER_USERNAME, DOCKER_PASSWORD,
   HEROKU_API_KEY (Values are DOCKER_USERNAME: your docker hub username; DOCKER_PASSWORD: your docker hub password;
   HEROKU_API_KEY: API key from the heroku app)

### GitHub Notes:  Set the action secrets repository in: -> settings -> actions -> secrets

### Heroku Notes: Get the heroku API key from account in: -> applications -> create authorization button

#### Change GitHub Actions Workflows for Prod

4. Change line 42 to have your docker repo address in: .github/workflows/prod.yml
5. change lines 58 to have your heroku app name in: .github/workflows/prod.yml
6. change line 59 to have your heroku email in: .github/workflows/prod.yml
7. Push code to your local repo and check for any errors and fix any errors that appear when the workflow is running.
   You can check the workflow in the
   actions.

## Running Locally

1. To Build with docker compose:
   docker compose up --build
2. To run tests, Lint, and Coverage report use this command: pytest --pylint --cov

.pylintrc is the config for pylint, .coveragerc is the config for coverage and setup.py is a config file for pytest

### Future Notes and Resources

* https://flask-user.readthedocs.io/en/latest/basic_app.html
* https://hackersandslackers.com/flask-application-factory/
* https://suryasankar.medium.com/a-basic-app-factory-pattern-for-production-ready-websites-using-flask-and-sqlalchemy-dbb891cdf69f
* https://develie.hashnode.dev/exploring-flask-sqlalchemy-queries
* https://wtforms.readthedocs.io/en/3.0.x/
* https://bootstrap-flask.readthedocs.io/en/stable/
* https://flask-sqlalchemy.palletsprojects.com/en/2.x/
