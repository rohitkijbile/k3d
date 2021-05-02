# k3d The local kuberenetes cluster

### General information.

This needs docker as base for running the k3d infrastructure. In case you are using MAC/Windows then docker desktop is expected to be installed, if the linux distribution is used normal docker instalaltion is sufficiant.

### Installation on MAC
```
brew install k3d
```

### Usage

1 . Creating cluster
```
k3d cluster create <cluster_name>
```

2 . Create Cluster using config file.
```
k3d cluster create --config files/k3d.yaml
```
Note:- The k3d.yaml file has all the required information to spin-up the cluster.
Minimal required filelds are 
"image" -> which defines the k8s cluster version.
"servers" -> This defines the control palane nodes.
"agents" -> This defines the worker plane nodes.

3 . Deleting cluster
```
k3d cluster delete <cluster_name>
```

