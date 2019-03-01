# Configure your local machine.

Once created the K8s cluster, download the config file from the digitalocean page

* my_k8s_cluster-kubeconfig.yaml *

Save this file in .kube/config, confirm is working with:

```
kubectl get nodes
	NAME                     STATUS    ROLES     AGE       VERSION
	distracted-banach-uif3   Ready     <none>    1h        v1.12.1
	distracted-banach-uifn   Ready     <none>    1h        v1.12.1

```
