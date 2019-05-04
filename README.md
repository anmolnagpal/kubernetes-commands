<p align="center"><img src="https://i.imgur.com/IYVX7a8.png" /></p>

What is Kubernetes?

> Kubernetes is a platform for managing containerized workloads. Kubernetes orchestrates computing, networking and storage to provide a seamless portability across infrastructure providers

## Cluster Info
```yaml
> kubectl config
> kubectl cluster -info
> kubectl get componentstatuses
```

## Viewing Resource Information

#### Nodes
```bash
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
```bash
> kubectl get ns
> kubectl get ns -o yaml
> kubectl describe ns
```

#### Services
```bash
> kubectl get svc
> kubectl describe svc
> kubectl get svc -o wide
> kubectl get svc -o yaml
> kubectl get svc --show-labels
```

#### Deployments
```bash
> kubectl get deploy
> kubectl describe deploy
> kubectl get deploy -o wide
> kubectl get deploy -o yaml
```

#### ConfigMaps
```bash
> kubectl get cm
> kubectl get cm -n=[namespace]
> kubectl get cm -n=[namespace] -o yaml 
> kubectl get cm --all -namespaces
> kubectl get cm --all -namespaces -o yaml
```

#### Logs
```bash
> kubectl logs [pod_name]
> kubectl logs [pod_name] -n=[namespace]
> kubectl logs --since=1h [pod_name]
> kubectl logs --tail=20 [pod_name]
> kubectl logs -f -c [container_name][pod_name]
> kubectl logs [pod_name] > pod.log
```

#### Secrets
```bash
> kubectl get secrets
> kubeclt get secrets -n=[namespace]
> kubectl get secrets -n=[namespace] -o yaml 
> kubectl get secrets --all -namespaces
> kubectl get secrets -o yaml
```

#### ReplicaSets
```bash
> kubectl get rs
> kubectl describe rs
> kubectl get rs -o wide
> kubectl get rs -o yaml
```
