# Kubernetes with K0s

Tutorial: https://www.albertcoronado.com/2021/06/08/tutorial-kubernetes-i/

## Commands

### Basic:

kubectl apply -f miapp.yml

kubectl cluster-info

kubectl get nodes

kubectl describe node <name>

kubectl top node <name>

kubectl cordon/uncordon <name>

kubectl drain <name>

### Pods:

kubectl get pods

kubectl describe pod <name>

kubectl top pod <name>

kubectl exec <pod> -c <contenedor> <comando>

kubectl cp /tmp/foo <pod-name>:/tmp/bar -c <container-name>

kubectl logs <pod-name> -c <container-name>

kubectl port-forward --address 0.0.0.0 pod/<pod-name> <host-port>:<pod-port>

### Namespaces:

kubectl get namespaces

kubectl create namespace <nombre>

kubectl apply -f pod.yaml --namespace=<nombre>

kubectl config set-context --current –namespace=default
