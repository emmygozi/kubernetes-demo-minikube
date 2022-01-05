# README

- type: LoadBalancer in mongo-express makes it an external service.
- Also nodePort: 30000 specifies the external port. The range allowed is from 30000 - 32767

kubectl apply -f mongo-secret.yaml

kubectl apply -f mongo.yaml

kubectl apply -f mongo-configmap.yaml - apply mongo configmap yaml configuration. Configmap is like a file where
you store cofigurations for other objects. Used for shared resources like database URL that might not be secrets

kubectl apply -f mongo-express.yaml - apply mongo express yaml configuration

kubectl get pods - get all running pods. You can and | grep podName

minikube service mongo-express-service -asign mongo-express on external port 30000 to an external IP address as shown below

| NAMESPACE   | NAME                    | TARGET PORT   | URL                          |
| ----------- | ----------------------- | ------------- | ---------------------------- |
| default     | mongo-express-service   | 8081          | http://172.29.35.176:30000   |
| 
