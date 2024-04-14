# CLO835-Final-Project-Group12
## Deployment of 2-tiered web application to managed K8s cluster on Amazon EKS, with pod auto-scaling and deployment automation.
CLO835-Final Project -Group12





### Commands to run the application
```bash
cd mainfest
kubectl create namespace final
kubectl apply -f service-account.yaml -n final
kubectl apply -f secret.yaml -n final
kubectl apply -f mysql_deployment.yaml -n final
kubectl apply -f mysql_clusterip.yaml -n final
kubectl apply -f ConfigMap.yaml -n final
kubectl apply -f webapp_deployment.yaml -n final
kubectl apply -f webapp_lb.yaml -n final
kubectl apply -f hpa_config.yaml -n final
