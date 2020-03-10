# project-ml-microservices-kubernotes

[![CircleCI](https://circleci.com/gh/dojutsu-user/project-ml-microservices-kubernotes.svg?style=svg)](https://circleci.com/gh/dojutsu-user/project-ml-microservices-kubernotes)

## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API.

You are given a pre-trained, sklearn model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, app.py—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

## Project Tasks

Your project goal is to operationalize this working, machine learning microservice using kubernetes, which is an open-source system for automating the management of containerized applications. In this project you will:

* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested.

## Steps (Without Docker)

* Create a virtual environment and activate it:
    ```
    $ make setup
    ```
* Install all the dependencies:
	```
    (.devops) $ make install
    ```
* Start the webapp
	```
    (.devops) $ python app.py
	```

## Steps (With Docker)

* Install [Docker](https://docs.docker.com/install/).
* Run the bash script:
	```
    $ bash run_docker.sh
    ```
## Steps (With Kubernetes)

* Install [Minikube](https://kubernetes.io/docs/tasks/tools/install-minikube/).
* Start Minikube:
	```
    $ minikube start
    ```
* Run the bash script:
	```
    bash run_kubernetes.sh
    ```

## Files

* `docker_out.txt`: Logs generated when the webapp is deployed with docker.
* `kubernetes_out.txt`: Logs generated when the webapp is deployed with kubernetes.
* `make_prediction.sh`: Bash script to make POST request to `localhost:8000` to make prediction with sample input.
* `run_kubernetes.sh`: Bash script to start the webapp with kubernetes.
* `run_docker.sh`: Bash script to start the webapp with docker.
* `upload_docker.sh`: Bash script to upload docker image to docker hub.
