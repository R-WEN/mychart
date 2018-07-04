Fork From [`pingcap`] (http://download.pingcap.org/tidb-operator-charts-latest.tar.gz)

***

This is the chart package for Helm

## Requirements

* kubernetes >= v1.7
* feature gates [`TaintBasedEvictions`](https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/#taint-based-evictions) enabled
* [RBAC](https://kubernetes.io/docs/admin/authorization/rbac) enabled (optional)

## Install Helm

1. Go to [release page](https://github.com/kubernetes/helm/releases) to download the latest helm binary package
2. Extract helm and copy the binary to your $PATH
3. Install Helm server Tiller: `helm init`
4. Check Tiller is up and running: `kubectl get po,svc -l name=tiller -n kube-system`

## Deploy tidb-operator

* Modify vars in tidb-operator/values.yaml
* Install tidb-operator: `helm install tidb-operator`

## Deploy a tidb-cluster

* Modify vars in tidb-cluster/values.yaml
* Install a tidb-cluster in k8s: `helm install tidb-cluster`
