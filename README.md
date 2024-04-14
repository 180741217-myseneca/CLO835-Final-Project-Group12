# CLO835-Final-Project-Group12
## Deployment of 2-tiered web application to managed K8s cluster on Amazon EKS, with pod auto-scaling and deployment automation.
CLO835-Final Project -Group12





### Commands to run the application
```bash
cd mainfest
kubectl create namespace final
kubectl apply -f ServiceAccount.yaml -n final
kubectl apply -f mysql_secrets.yaml -n final
kubectl apply -f configmaps.yaml -n final
kubectl apply -f pvc -n final
kubectl apply -f mysqldeployment.yaml -n final
kubectl apply -f mysqlclusterip.yaml -n final
kubectl apply -f web_nodeport.yaml -n final
kubectl apply -f WebappDeployment.yaml -n finaL
kubectl apply -f webapp_lb.yaml -n final
kubectl apply -f hpa_config.yaml -n final
