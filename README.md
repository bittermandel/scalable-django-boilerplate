# Scalable Boilerplate

## Highly opinionated boilerplate for Django

* Docker Compose as development environment
* CircleCI as testing environment
* Kuberenetes on GCE as production environment

### Get up and running
1. Log in to GCloud:
```gcloud auth application-default login```
2. Create GCloud cluster:
```gcloud container cluster create --num-nodes=2 --machine-type=g1-small```
2. Create ConfigMap from application specific .env file:
```kubectl create configmap django-config --from-file=django=application/.env```