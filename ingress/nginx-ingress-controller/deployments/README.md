# Installation

Create a namespace and a service account for the Ingress controller:
```
kubectl apply -f common/ns-and-sa.yaml
```
Create a cluster role and cluster role binding for the service account:
```
kubectl apply -f rbac/rbac.yaml
```
Create a secret with a TLS certificate and a key for the default server in NGINX:
```
kubectl apply -f common/default-server-secret.yaml
```
Create a config map for customizing NGINX configuration:
```
kubectl apply -f common/nginx-config.yaml
```
nginx-ingress class
```
kubectl apply -f common/ingress-class.yaml
```
DaemonSet 
```
kubectl apply -f daemon-set/nginx-ingress.yaml
```





