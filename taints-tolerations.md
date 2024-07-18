kubectl taint nodes node01 app=blue:NoSchedule

// taint-effect = NoSchedule | PreferNoSchedule | NoExecute (will evict running pods without the correct toleration

// remove the taint
kubectl taint node controlplane node-role.kubernetes.io/control-plane:NoSchedule-
