# Creating cluster with terraform 

For this first part, a K8s cluster will be created with terraform in DigitalOcean.

Execute the terraform code. Is assumed a DigitalOcean account is already setup and ready. 

```
terraform init
terraform plan
terraform apply
```

terraform code
```
provider digitalocean{}

resource "digitalocean_kubernetes_cluster" "my_cluster" {
    name = "my_k8s_cluster"
    region = "nyc1"
    version = "1.12.1-do.2"

    node_pool {
        name       = "node_pool_example"
        size       = "s-1vcpu-2gb"
        node_count = 2
        tags       = ["k8s", "learning"] 
    }   
}
```

This code will create a kubernetes cluster with two nodes in the "nyc1" region. 
