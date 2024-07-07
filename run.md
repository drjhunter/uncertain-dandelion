kubectl run nginx2 --image=nginx

kubectl run nginx2 --image=nginx --dry-run=client -o yaml

kubectl run nginx2 --image=nginx --dry-run=client -o yaml > my-deployment.yaml

kubectl run custom-nginx --image=nginx --port=8080

kubectl run custom-nginx --image=nginx --port=8080 --expose=true # creates clusterip service
