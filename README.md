# Microservicios-con-Kubernetes-php-mysql
Microservicios con Kubernetes, docker, php y MySql 

**NTRAR AL POD** 

kubectl exec -it webapp-6b87bc488d-tglb7 -- bash

minikube start

# Dentro de la carpeta webapp

eval $(minikube docker-env)    

minikube ip

docker build -t ip-nueva:5000/webapp:latest .

## Reviso que se ha creado la imagen correctamente en otra terminal

minikube ssh

minikube images

kubectl apply -f webApp-deployment.yml

kubectl apply -f webApp-service.yml

# Dentro de la carpeta mysql

kubectl apply -f mysql-configmap.yml

kubectl apply -f webApp-pv.yml

kubectl apply -f webApp-pvc.yml

kubectl apply -f webApp-deployment.yml

kubectl apply -f webApp-service.yml

kubectl port-forward service/webApp 8080

# Dentro de la carpeta phpmyadmin

kubectl apply -f phpmyadmin-deployment.yml

kubectl apply -f phpmyadmin-deployment.yml

kubectl port-forward service/phpmyadmin 8080:8080