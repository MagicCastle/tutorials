# Configure your cluster - part 2

## instances

The `instances` variable is a map that defines the virtual machines that will compose
the cluster, where the keys define the hostnames and the values are the attributes
of the virtual machines.

Each instance is identified by a unique hostname. An instance's hostname is composed as
the key followed by the (1-based) its index. The following map:
```hcl
instances = {
  mgmt     = { type = "p2-4gb", tags = [...] },
  login    = { type = "p2-4gb",     count = 1, tags = [...] },
  node     = { type = "c2-15gb-31", count = 2, tags = [...] },
  gpu-node = { type = "gpu2.large", count = 3, tags = [...] },
}
```
will spawn instances with the following hostnames:
```
mgmt1
login1
node1
node2
gpu-node1
gpu-node2
gpu-node3
```

Two attributes are expected to be defined for each instance:
1. `type`: cloud provider name for the combination of CPU, RAM and other features of the virtual machine;
2. `tags`: list of labels that defines the role of the instance.

:::{admonition} Notes on tags
Tags are used in the Terraform
code to identify if devices (volume, network) need to be attached to an instance, while in Puppet code tags are used to identify roles of the instances.
:::

Leave this variable to its current value for this tutorial.

