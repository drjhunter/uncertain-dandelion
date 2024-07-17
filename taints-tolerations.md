kubectl taint nodes node01 app=blue:NoSchedule

// taint-effect = NoSchedule | PreferNoSchedule | NoExecute (will evict running pods without the correct toleration
