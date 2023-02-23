# Creation of a mongodb web app ,  

# To do that , 

# Create a config map for mongodb endpoint 

# Secret for mongodb user name and password 

# Create a deployment and a service for mongodb app with internal service 

# define components for mongo an webapp inorder to pass the secret and comfigmap data into pods

#create a deployment and service for our own web app with external service 

# to create a base64 mongo user

echo -n mongouser | base64

# to create a base64 mongo password

echo -n mongopassword | base64
 
 ####  to deploy this applicatio after modifying the username and password, run the below commands

 kubectl get pods >to ensure that a container is not previously running in your pipeline at the time of your deployments

 # creat all the configuration files that are listed in the mongo-webapp-deployment

 # apply the confiq files starting with the mongo-config file to store the database credentials that will be picked at runtime.

 kubectl apply -f mongo-config.yaml

kubectl apply -f mongo-secret.yaml

kubectl apply -f mongo.yaml

kubectl apply -f webapp.yaml

# check if all components have been created

kubectl get all

# to view your config maps/ secrets

kubectl get secret / kubectl get congig map

# to get help of all kubectl sub commands

kubectl get --help

# to get detail description of a component

kubectl describe service service name      
eg: kubectl describe service mongo-service

# to check your container logs

kubectl logs container name

# to validate if the service is accessible from the browser

kubectl get service  or kubectl get svc

# to get the ip address of the node with wider descriptions

kubectl get node -o wide


