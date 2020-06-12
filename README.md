### Description
Deploy a WordPress instance with High Availability with persistence volumes to store both static and database storage requirements. 

The default replication is set to 1 with max to 3 controlled by Horizontal Pod Autoscaler (HPA).

The deployment is done on minikube with single Node instance
### Requirements
- Existing default storage policy (available in minikube)
- Metrics addon enabled for HPA ("minikube addons enable metrics-server")

#### Deployment
- Move to the directory containing the "kustomization.yml" file
- Execute: kubectl apply -k ./

#### Access
- The instance is accessible by NodePort at 30000
- Get the IP: minikube ip
- Access at: <minikube_ip>:30000
#### Clean Up
- Execute: kubectl delete -k ./
