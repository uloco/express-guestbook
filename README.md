# Express Guestbook Kubernetes Example

## Build the container

```
npm install
docker build -t guestbook-express .
```

## Deyploy to minikube

Make sure minikube is installed, then run:

```
minikube start
eval $(minikube completion zsh)
kubectl apply -f ./deployment.yaml
minikube service guestbook-express-service
```
