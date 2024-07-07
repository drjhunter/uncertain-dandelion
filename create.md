kubectl create service clusterip redis-service --tcp=6379:6379

kubectl create deployment webapp --image=kodekloud/webapp-color --replicas=3
