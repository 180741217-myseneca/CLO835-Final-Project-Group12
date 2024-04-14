# CLO835-Final-Project-Group12
## Deployment of 2-tiered web application to managed K8s cluster on Amazon EKS, with pod auto-scaling and deployment automation.

### Prerequsites
```bash
Create image add put that image to s3 bucket
webapp,mysql image move to the ecr using github workflow

```

### EKS cluster build 
```bash
export AWS_ACCESS_KEY_ID="In your AWS details"
export AWS_SECRET_ACCESS_KEY="In your AWS details+"
export AWS_SESSION_TOKEN="In your AWS details"

Check kubectl version -kubectl version --client
Check eksctl version -kubectl

In version not found install using below.
Install kubectl - https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html
Install eksctl  - https://docs.aws.amazon.com/eks/latest/userguide/eksctl.html

Check kubectl version -kubectl version --client
Check eksctl version -kubectl

Run the command
eksctl create cluster -f eks_config.yaml
```
### Commands to run the application in EKS cluster
```bash
cd mainfest
kubectl create namespace final
kubectl apply -f ServiceAccount.yaml -n final
kubectl apply -f mysql_secrets.yaml -n final
kubectl apply -f configmaps.yaml -n final
kubectl apply -f pvc.yaml -n final
kubectl apply -f mysqldeployment.yaml -n final
kubectl apply -f mysqlclusterip.yaml -n final
kubectl apply -f web_nodeport.yaml -n final
kubectl apply -f WebappDeployment.yaml -n finaL
kubectl apply -f webapp_lb.yaml -n final
