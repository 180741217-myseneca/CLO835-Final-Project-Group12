# CLO835-Final-Project-Group12
## Deployment of 2-tiered web application to managed K8s cluster on Amazon EKS, with pod auto-scaling and deployment automation.
CLO835-Final Project -Group12





### Commands to run the application
```bash
cd mainfest
kubectl create namespace final
kubectl apply -f ServiceAccount.yaml -n final
kubectl apply -f mysql_secret.yaml -n final
kubectl apply -f mysqldeployment.yaml -n final
kubectl apply -f mysqlclusterip.yaml -n final
kubectl apply -f Configmaps.yaml -n final
kubectl apply -f Configmaps.yaml -n finaL
kubectl apply -f web_nodeport.yaml -n final
kubectl apply -f webapp_lb.yaml -n final
kubectl apply -f hpa_config.yaml -n final
