# k8s

To run the exam

``` 
k3d cluster create  -p "8081:80@loadbalancer" --agents 2 
    
# this step is functional for using mac. This is simply exposing the port 80 from the load balancer into the 8081 on the host computer

kubectl apply -f my-secret-eval.yml     
kubectl apply -f my-deployment-eval.yml 
kubectl apply -f my-service-eval.yml      
kubectl apply -f my-ingress-eval.yml      