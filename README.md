# rhcam-pull-mode
Red Hat Advanced Cluster Management for Kubernetes pull mode

## Installation

### Managed Clusters
- Install Openshift GitOps operator
```
oc apply -f ./cluster-configuration/multi-cluster-hub.yaml
```
- Configure Openshift GitOps
```
oc apply -f ./cluster-configuration/argocd-cluster-role-binding.yaml
```

### Cluster Hub

- Install RHACM operator
- Install Openshift GitOps operator
- Configure MultiClusterHub
```
oc apply -f ./cluster-configuration/multi-cluster-hub.yaml
```
- Configure Openshift GitOps
```
oc apply -f ./cluster-configuration/argocd-cluster-role-binding.yaml
```
- Create ManagedClusterSet
```
oc apply -f ./cluster-configuration/managed-cluster-set.yaml
```
- Import managed clusters
- Create ManagedClusterSetBinding
```
oc apply -f ./cluster-configuration/managed-cluster-set-binding.yaml
```
- Create Placement
```
oc apply -f ./cluster-configuration/placement.yaml
```
- Create GitOpsCluster
```
oc apply -f ./cluster-configuration/gitops-cluster.yaml
```

## Deploy Argo CD ApplicationSet

```
oc apply -f ./cluster-configuration/gitops-cluster.yaml
```