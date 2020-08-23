# simple-microservice - Blog
This is a Blog project handled with different microservices created in node.js and a client side built in react.
For learning purposes, a simple event-bus has been manually implemented to manage data between services as a means to prevent dependencies.
Deployment is done with Docker and Kubernetes in a very basic way in localhost.

## Recomendations
Install docker hub on your computer via its [website](https://www.docker.com/)
Activate kubernetes in the settings of docker-hub

## Microservices
- Posts (on port 4000)
- Comments (on port 4001)
- Query (on port 4002)
- Moderation (on port 4003)
- Event-bus (on port 4005)

## Client
- React app (on port 3000)

## Technologies
- Node.js
- React
- Docker
- Kubernetes

## Dependencies
- express
- nodemon
- axios
- cors

## Commands

### Start the service/client
- npm install
- npm start

### Start the docker
- docker build . ( or docker build -t <docker_id>/<pod_name> . )
- docker push <docker_id>/<pod_name>
- docker ps --all
- docker run <image>

### Kubernetes (inside infra folder)
- kubectl apply -f <pod_file_name.yaml>
- kubectl get pods
- kubectl exec -it <pod_name> <command>
- kubectl logs <pod_name>
- kubectl describe pod <pod_name>
- kubectl delete pod <pod_name>

- kubectl apply -f <deployment_file_name.yaml>
- kubectl get deployments
- kubectl describe deployment <deployment_name>
- kubectl delete deployment <deployment_name>
- kubectl rollout restart deployment <deployment_name>
