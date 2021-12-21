# Shyavappa PHP Sample app

Used tools:

- PHP
- Docker
- Kubernetes

## Steps to deploy the app on kubernetes

- Clone the repo

```sh
git clone
cd assignment_php-code
```

- Build the image and push it to your docker registry

```sh
docker build -t <docker_repo/your_image_name>:<tag> .
docker image push <docker_repo/your_image_name>:<tag>
```
Added the docker hub credentials using below commands

kubectl create secret docker-registry dockerhub --docker-server=https://hub.docker.com --docker-username=******** --docker-password=********* --docker-email=*@*.com
- Deploy the components in k8s/ folder to your kubernetes cluster

used this secret in deployment.yaml file.

```sh
kubectl apply -f ./k8s/
```
