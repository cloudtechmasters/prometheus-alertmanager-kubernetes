# prometheus-alertmanager-kubernetes

# Pre-Requisites:
    EKS-Cluster
# Deploy Node Exporter 
    kubectl apply -f node-exporter
# Deploy kube-state-metrics
    kubectl apply -f kube-state-metrics
# Deploy alertmanager
    kubectl apply -f alertmanager
# Deploy prometheus
    kubectl apply -f prometheus
# Note:
  Here I kept two rules: (we can get alaram)
  1. CPU Utilization High for Nodes
  2. Pod status Pending/Unknown
# Alaram1: Connect to node and try to increase CPU Utilization, will get Alaram
# Alaram2: Deploy nginx
    kubectl apply -f nginx-deployment.yml
  Nginx Pod status will be under pending state, So will get Alaram
