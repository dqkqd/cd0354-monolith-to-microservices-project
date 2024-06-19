# Screenshots

To help review your infrastructure, please include the following screenshots in this directory::

## Deployment Pipeline

### DockerHub containers

![docker-hub-image](images/dockerhub.png)

### CircleCI successful build and deploy job

![circleci-pipelines](images/circleci-pipelines.png)

## Kubernetes

* To verify Kubernetes pods are deployed properly

```bash
kubectl get pods
```

![kubectl-get-pods](images/kubectl-get-pods.png)

* To verify Kubernetes services are properly set up

```bash
kubectl describe services
```

![kubectl-describe-services-1](images/kubectl-describe-services-1.png)
![kubectl-describe-services-2](images/kubectl-describe-services-2.png)

* To verify that you have horizontal scaling set against CPU usage

```bash
kubectl describe hpa
```

![kubectl-describe-hpa](images/kubectl-describe-hpa.png)

* To verify that you have set up logging with a backend application

```bash
kubectl logs {pod_name}
```

![kubectl-logs](images/kubectl-logs.png)
