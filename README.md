# k8s-sns-ia

MetalLB
```
kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.13.10/config/manifests/metallb-native.yaml

kubectl apply -f metallb-values.yaml
```

Traefik
```
helm repo add traefik https://traefik.github.io/charts
helm repo update

helm install traefik traefik/traefik -f traefik-values.yaml --namespace kube-system
```
