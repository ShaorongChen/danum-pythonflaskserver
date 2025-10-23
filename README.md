# Python Flask Server

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/flask-000000?style=for-the-badge&logo=flask&logoColor=white)

This project is a Python Flask server that serves as the backend for a microservices architecture.

## Features

- Simple Flask application
- Dockerized deployment
- Multi-stage build for efficient containerization

## Getting Started

### Prerequisites

- Docker
- Python 3.13

### Installation

1. Clone the repository
2. Build the Docker image:
   ```bash
   docker build . -t us.icr.io/${SN_ICR_NAMESPACE}/helloworld2
   ```
3. Push the container:
   ```bash
   docker push us.icr.io/${SN_ICR_NAMESPACE}/helloworld2
   ```
4. Push the container:
   ```bash
   ibmcloud ce application create --name helloworld2 --image us.icr.io/${SN_ICR_NAMESPACE}/helloworld2 --registry-secret icr-secret --port 5000
   or
   ibmcloud ce application update --name helloworld2 --image us.icr.io/${SN_ICR_NAMESPACE}/helloworld2 --registry-secret icr-secret --port 5000
   ```
## Usage

Visit `http://theURLFromIbmCeCli` to see the application in action.