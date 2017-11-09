Create Redis Pod
kubectl create -f redis.yml

Create Node application Front end deployment with three replicas
kubectl create -f node_fe.yml

Expose Redis to the FE via externl IP
kubectl expose pod redis --type=externalIP

Expose Node FE via Node Port
kubectl expose deployment node_fe --type=NodePort
