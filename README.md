What is Kubernetes?
> Kubernetes is a platform for managing containerized workloads. Kubernetes orchestrates computing, networking and storage to provide a seamless portability across infrastructure providers

## ViewingResource Information
#### Nodes
```yaml
> kubectl get no
> kubectl get no -o wide
> kubectl describe no
> kubectl get no -o yaml
> kubectl get node --selector=[label_name]
> kubectl get nodes -o jsonpath='{.items[*].status.addresses[?(@.type=="ExternalIP")].address}'
> kubectl top node [ node_name]
```
#### Pods
```bash
> kubectl get po
> kubectl get po -o wide
> kubectl describe po
> kubectl get po --show -labels
> kubectl get po -l app=nginx
> kubectl get po -o yaml
> kubectl get pod [pod_name] -o yaml --export
> kubectl get pod [pod_name] -o yaml --export > nameoffile.yaml
> kubectl get pods --field-selector status.phase=Running
```
#### Namespaces
```sh
> kubectl get ns
> kubectl get ns -o yaml
> kubectl describe ns
```
