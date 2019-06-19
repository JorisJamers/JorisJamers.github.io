# Private GKE Cluster on Google Cloud Platform

While the default Google Kubernetes Engine cluster on Google Cloud Platform is open with multiple public endpoints, we might not want a cluster that is publicly available.

In this project I did some research to how we are able to create a private GKE cluster without any public endpoint. The setup that I created had a bastion host in front of the cluster. With this bastion we would be able to connect via SSH to the bastion and connect to the GKE cluster. This is much easier to decide who can connect to the cluster or who just needs to consume the cluster (e.g. deploy services, deployments, …)

I ended up putting all this infrastructure in Terraform. The Terraform code would deploy the GKE private cluster, the bastion host and all the other resources we would need to make this work (e.g. network, subnetwork, NAT router, firewall, …). Of course, with Terraform best practices to create re-useable modules.

#### Tools & Technologies

* Terraform
* Google Cloud Platform
* Google Kubernetes Engine
* Gitlab
* Kubernetes 

[Back](../projects.md)

[Home](../../index.md)
