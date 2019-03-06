# Installing our first chart
We'll create a new namespace with:

```
kubectl create namespace mygitlab
```

The above command, sets up a new namespace in your Kubernetes cluster with the name "mygitlab". Next 
we'll use Helm to install GitLab into this namespace: 

```
helm install -n mygitlab --name git stable/gitlab-ce --set externalUrl=http://<yourURL>.com
```

To get the IP execute the next command: 

```
kubectl get services --namespace mygitlab git-gitlab-ce -o jsonpath='{.status.loadBalancer.ingress[0].ip}'
```
