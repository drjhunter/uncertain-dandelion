kubectl run nginx2 --image=nginx
kubectl run nginx2 --image=nginx --dry-run=client -o yaml
kubectl run nginx2 --image=nginx --dry-run=client -o yaml > my-deployment.yaml
