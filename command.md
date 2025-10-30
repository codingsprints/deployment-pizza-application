```bash
kubectl apply -f ./deployment.yaml

kubectl get deployment

kubectl get service (svc)

kubectl get pods  # docker container

kubectl logs <podsID>

kubectl delete -f ./deployment.yaml

kubectl get deploy

kubectl get nodes -o wide
kubectl get pod -o wide
```

## auth service

<!-- # deployment auth service -->

```bash
kubectl apply -f ./api-env-secert.yaml

kubectl apply -f ./auth-private-key-secret.yaml

kubectl apply -f ./jwks-cm.yaml

kubectl get cm (configMap)
kubectl get secret

kubectl apply -f ./deployment.yaml

kubectl get pods
kubectl logs <podsID>

kubectl get nodes -o wide
kubectl get pod -o wide

kubectl delete -f ./deployment.yaml

kubectl port-forward svc/argocd-server -n argocd 8080:443
```

- note: 'Network load balancer' same as 'application load balancer'

```bash
# nginx
kubectl get deploy -n ingress-nginx #(list namespace)
kubectl get pod -n ingress-nginx #(list pod)

# apply nginx
kubectl apply -f ./auth-ingress.yaml
kubectl get svc #(service)
```

## argo CD

```bash
kubectl create namespace argocd

kubectl get ns

kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

kubectl get pods -n argocd

kubectl port-forward svc/argocd-server -n argocd 8080:443

kubectl get endpoints
```

## catalog-service

```bash
kubectl apply -f .\catalog-secret.yaml

kubectl apply -f ./deployment.yaml

kubectl apply -f .\order-secret.yaml
```
