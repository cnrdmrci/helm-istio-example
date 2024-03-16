
## Create namespaces

```
kubectl create namespace helm-istio-dev
kubectl create namespace helm-istio-prod
```

## Activate istio
```
kubectl label namespace helm-istio-dev istio-injection=enabled
kubectl label namespace helm-istio-prod istio-injection=enabled
```
## Open minikube External
```
minikube tunnel
```

## Create with helm
```
helmfile sync
```

## Test
```
curl localhost:80/v1
curl localhost:80/v2
```