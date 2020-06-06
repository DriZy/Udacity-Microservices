[![GitHub](https://circleci.com/gh/DriZy/Udacity-Microservices.svg?style=svg)](https://app.circleci.com/pipelines/github/DriZy/Udacity-Microservices)

## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`
4. Make predictions: `./make_predictio.sh`
5. Upload docker image: `upload_docker.sh`

### Kubernetes Steps

* Setup and Configure Docker locally `https://docs.docker.com/desktop/`
* Setup and Configure Kubernetes locally `https://kubernetes.io/docs/tasks/tools/install-kubectl/`
* Setup and Configure Minikube locally `https://kubernetes.io/docs/tasks/tools/install-minikube/`
* Run `minikube start` to create a cluster
* Run `kubectl config view` to check if the cluster is running
* Run via kubectl

### Details on files

* `Makefile` Includes instructions on environment setup and lint tests
* `requirements.txt` Contains all the dependencies
* `app.py` Is the python flask app
* `run_docker.sh` Builds the docker image and run it on the specified port
* `run_kubernetes.sh` Runs the flask app via kubernetes
* `make_predictio` Makes prediction for housing prices in Boston.
* `upload_docker.sh` Uploads the docker image to the specify docker repository 
* `.circleci/config.yml` Contains the configurations needed for the pipeline on circleci

