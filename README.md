[![CircleCI](https://circleci.com/gh/sakshi-kst/Operationalize-an-ML-Microservice-API/tree/master.svg?style=svg)](https://circleci.com/gh/sakshi-kst/Operationalize-an-ML-Microservice-API/tree/master)

## Project Overview

In this project, we apply the skills acquired in the course to operationalize a Machine Learning Microservice API. 

We have a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. To know more about the data, which was initially taken from Kaggle, we can visit [the data source site](https://www.kaggle.com/c/boston-housing). This project tests our ability to operationalize a Python flask app — `app.py` that serves out predictions about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

The project's goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project, we:
* Test the project code using linting
* Complete a Dockerfile to containerize this application
* Deploy the containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that the code has been tested

We can find the detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase the ability to operationalize production microservices.**

---

### Project Contents

* .circleci: Contains the CircleCI config file
* model_data: Contains the Boston housing dataset and prediction
* output_txt_files: Contains prediction output files after running Docker and Kubernetes
* app.py: Main Flask based application
* Dockerfile
* make_prediction.sh: Runs prediction based on a given set of inputs
* Makefile
* requirements.txt: Contains the libraries to be installed for running Flask application
* run_docker.sh: Builds and runs the Docker image of Flask application
* run_kubernetes.sh: Runs the Docker container with Kubernetes
* upload_docker.sh: Pushes Docker image to Docker repository

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies
* Run `make lint` to test the project code using linting

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`
4. Make predictions: `./make_prediction.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally using Minikube
* Create Flask app in Container
* Run via kubectl
