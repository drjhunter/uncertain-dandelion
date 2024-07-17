// to patch an existing pod
curl --header "Content-Type:application/json" --request POST --data '{<JSON data for binding object>}' http://$SERVER/api/v1/namespaces/default/pods/$PODNAME/binding/

pod-bind-definition.yaml // file content passed to api call
apiVersion: v1
kind: Binding
metadata:
  name: nginx
target:
  apiVersion: v1
  kind: Node
  name: node01


// alternatively, to create a pod and schedule it in one go, hard-code the node in the deployment file
nginx.yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx
spec:
  containers:
  -  image: nginx
     name: nginx
  nodeName: node01
