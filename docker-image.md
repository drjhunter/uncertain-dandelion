FROM Ubuntu
ENTRYPOINT["sleep"]
CMD["5"]


# customise entrypoint and cmd from the pod definition

apiVersion: v1
kind: Pod
metadata:
  name: ubuntu-sleeper-pod
spec:
  containers:
    - name: ubuntu-sleeper
      image: ubuntu-sleeper
      command: ["sleep2.0"] # maps to ENTRYPOINT
      args: ["10"] # maps to CMD
