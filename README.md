# Udagram Image Filtering Application

Udagram is a simple cloud application developed alongside the Udacity Cloud Developer Nanodegree. It allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering microservice.

The project is split into two parts:

1. Frontend - Angular web application built with Ionic Framework
2. Backend RESTful API - Node-Express application

Please refer to [report](screenshots/README.md) for screenshots and evidences.

1. Containers and Microservices
    - Divide an application into microservices:
        - `/feed` and `/user` are endpoints are separated into `/udagram-api-feed` and `/udagram-api-user` folders respectively
    - Build and run a container image using Docker:
        - `Dockerfile` are included in each of the `udagram-*` folder
        - DockerHub screenshot is provided in `screenshots/images/dockerhub.png`
2. Independent Releases and Deployments
    - Project includes a `.circleci/config.yml` file
    - CircleCI pipeline screenshot is included
3. Service Orchestration with Kubernetes
    - Deploy microservices using a Kubernetes cluster on AWS:
      - Screenshot of running pods is provided in `screenshots/images/kubectl-get-pods.png`
      - Screenshots of services are provided in `screenshots/images/kubectl-describe-services-1.png` and `screenshots/images/kubectl-describe-services-2.png`
    - Use a reverse proxy to direct requests to the appropriate backend:
      - Screenshot of running proxy is provided in `screenshots/images/kubectl-describe-services-2.png`
    - Configure scaling and self-healing for each service:
      - Specify two replicas for `udagram-api-feed` in `deploy/backend-feed-deployment.yaml`
      - Screenshot of configured hpa is provided in `screenshots/images/kubectl-describe-hpa.png`
4. Debugging, Monitoring, and Logging
    - Use logs to capture metrics for debugging a microservices deployment
      - Screenshot of logging for pod `udagram-api-feed` is provided in `screenshots/images/kubectl-logs.png`
