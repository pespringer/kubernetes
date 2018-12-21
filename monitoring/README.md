helm install stable/grafana --name grafana --set persistence.enabled=true --set persistence.size=10G --set persistence.accessModes={ReadWriteOnce}

helm install     --name mon     --namespace monitoring     -f custom-values.yaml     coreos/kube-prometheus
