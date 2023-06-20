# Doctor Training Day


# Environment Pre-Requirements

### Docker

* Environment requires Docker for k3d (dockerized k3s)

### HashiCorp Consul Enterprise

* HashiCorp Consul Enterprise license required.
  * Place in `./license`

### K3d

* K3d is a dockerized version of K3s, which is a simple version of Rancher Kubernetes.
* K3d is used for the platform Consul on Kubernetes portion of this environment.
* Installation instructions [HERE](https://github.com/k3d-io/k3d#get)

### Kubectl

* Installation instructions [HERE](https://kubernetes.io/docs/tasks/tools/)

### Helm

* Helm is used to configure and install Consul into Kubernetes.
* Installation instructions [HERE](https://helm.sh/docs/intro/install/)

### k9s 

* Highly recommended to get k9s to make navigating Kubernetes a lot easier.
* [https://github.com/derailed/k9s/releases](https://github.com/derailed/k9s/releases)

### HashiCorp consul-k8s CLI

* Installation instructions [HERE](https://developer.hashicorp.com/consul/docs/k8s/installation/install-cli#install-the-latest-version)

# Instructions to Execute Environment

### k3d configuration script 

* Build K3d Kubernetes clusters using the `k3d-config.sh` script:
  * `./k3d-config.sh -k8s-only`


### Delete Environment

* `./kill.sh -k3d`   (Only destroy the k3d clusters so they can be rebuilt without tearing down the entire docker environment.)

# Documentation

The Doctor Consul architecture (including visual diagram) and details are [HERE](docs/architecture.md)

### Zork Control Script

The `./zork.sh` script is a menu driven system to control various aspects of the Doctor Consul environment.
Docs: [HERE](docs/zork.md)

