# **Install Argo CD using manifests**

### kubectl create namespace argocd

### kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml


## **Access the Argo CD UI (Loadbalancer service)**

### kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "LoadBalancer"}}'

## **Get the Loadbalancer service IP**

### kubectl get svc argocd-server -n argocd