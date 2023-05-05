# Express Guestbook Kubernetes Example


### Features

* guestbook app written in express.js
* mongodb database
* entries are persisted between pod restarts / kills

## Build the container

```
npm install
docker build -t guestbook-express .
```

## Deploy to minikube

Make sure minikube is installed, then run:

```
minikube start
eval $(minikube completion zsh)
kubectl apply -f ./deployment.yaml
minikube service guestbook-express-service
```

