kubectl get pods --selector env=dev

kubectl get all --selector env=prod

// add a label to a node - only works for a simple case
kubectl label nodes node01 size=large

// add to pod definition
apiVersion:
kind: Pod
metadata:
  name: my-pod
spec:
  containers:
  - name: data-processor
    image: data-processor
  nodeSelector:
    size: large

// node affinity for more complex cases - replace nodeSelector element with:
<as previous>
  affinity:
    nodeAffinity:
      requiredDuringSchedulingIgnoredDuringExecution:
        nodeSelectorTerms:
        - matchExpressions:
          - key: size
            operator: In # NotIn, Exists
            values:
            - large
            - medium
