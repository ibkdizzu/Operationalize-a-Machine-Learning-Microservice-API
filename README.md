[![CircleCI](https://dl.circleci.com/status-badge/img/gh/ibkdizzu/Operationalize-a-Machine-Learning-Microservice-API/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/ibkdizzu/Operationalize-a-Machine-Learning-Microservice-API/tree/main)

## Project Overview

This project demonstrates how Devops can be used to i operationalize a Machine Learning Microservice API. 

Specifically a pre-trained, `sklearn` model to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on, is containerized using [Docker](https://www.docker.com) and [Kubernetes](https://kubernetes.io) and exposed via Flask API. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing).

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
* Set up virtual environment


## Section A - Setup Environment

* Fork the repo and clone it to your local workstation and change directory to the project files

  ```bash
   git clone https://github.com/udacity/DevOps_Microservices.git
   cd DevOps_Microservices/project-ml-microservice-kubernetes
   ```  
* Install/Update Python to version 3.7, Create and activate a virtual environment with same.
  ```bash
   python3 -m venv ~/.devops
   source ~/.devops/bin/activate
   ```
* Install dependencies by running `make install`
* (Optionally) Lint application (requires hadolint)
* Download the latest version of Docker for your environment 
* Install hadolint
* Install Kubectl, Minikube

## Section B - Run Docker Container
* Dockerfile: A Dockerfile contains recommended steps to build a docker image
      - Specify Docker image 
      - Copy the application into specified directory
      - Install all requirements
      - Expose Port 80 for the application to run
      - Run the application at container launch

### Running `app.py`
* From bash:  `python app.py`
* Run in Docker:  `./run_docker.sh`
* Run in Kubernetes:  `./run_kubernetes.sh`

### Upload to Docker Hub
* In the ./upload_docker.sh file, edit the dockerpath (line 8) and change the docker username to a personalized one
* To upload to docker hub, run ./upload_docker.sh

### Kubernetes Steps
* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
