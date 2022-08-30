[![CircleCI](https://dl.circleci.com/status-badge/img/gh/ibkdizzu/Operationalize-a-Machine-Learning-Microservice-API/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/ibkdizzu/Operationalize-a-Machine-Learning-Microservice-API/tree/main)

## Project Overview

This project demonstrates how Devops can be used to i operationalize a Machine Learning Microservice API. 

Specifically a pre-trained, `sklearn` model to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on, is containerized using [Docker](https://www.docker.com) and Kubernetes [Kubernetes](https://kubernetes.io) and exposed via Flask API. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing).

### Project Tasks

The tasks in this projects are listed below:
* Run a docker container
* Upload container into a public registry (ensure to sign up on hub.docker.com)
* Run the deployed application in a Kubernetes cluster
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

---
## Setup the Environment
* Python 3.7
* Docker
* Minikube
* Kubectl
* Virtual Environment


## Section A - Setup Environment

#### Step 1
* Fork the repo and clone it to your local workstation and change directory to the project files
  `git clone https://github.com/udacity/DevOps_Microservices.git`
   `cd DevOps_Microservices/project-ml-microservice-kubernetes`
 

Setup and Install all requirements
* Python 3.7
* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
