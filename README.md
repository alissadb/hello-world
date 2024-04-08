# Hello World API Project

This project is a simple API that responds with "Hello, World!" when accessed. It's designed to run in a Kubernetes environment and is a great starting point for learning about Kubernetes, Poetry, Pyenv, and Minikube.

## Prerequisites

Before you begin, ensure you have installed the following:
- [Poetry](https://python-poetry.org/docs/#installation)
- [Pyenv](https://github.com/pyenv/pyenv#installation)
- [Docker](https://www.docker.com/get-started/)
- [Kubernetes](https://kubernetes.io/docs/setup/) / [Deploy on Kubernetes with Docker Desktop
](https://docs.docker.com/desktop/kubernetes/)
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)

## Installation
⚠️ Warning: Currently, this project is only compatible with macOS and Linux.

1. Create a virtual environment using Poetry:

    ```bash
    poetry shell
    ```

2. Install all necessary packages:

    ```bash
    poetry install
    ```

3. Deploy the Kubernetes deployment and service:

    ```bash
    kubectl apply -f k8s/deployment.yaml
    kubectl apply -f k8s/service.yaml
    ```

## Usage

1. Start Minikube with the Docker driver:

    ```bash
    minikube start --driver=docker
    ```

2. Access the service:

    ```bash
    minikube service hello-world-service
    ```

3. Visit the URL provided by the above command to access the API. You should see a response of "Hello, World!".
