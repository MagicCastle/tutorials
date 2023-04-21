# Configure your cluster - part 1

In the `main.tf` file, there is a module named after your cloud provider,
i.e.: `module "openstack"`. This module corresponds to the high-level infrastructure
of your cluster.

The following sections describes some of the variables used to define
the deployed infrastructure and its configuration. The order of the variables
does not matter, but the following sections are ordered as the variables 
appear in the examples.

## source

The first line of the module block indicates to Terraform where it can find
the files that define the resources that will compose your cluster.
In the releases, this variable is a relative path to the cloud
provider folder (i.e.: `./aws`).

Leave this variable to its current value for this tutorial.

## config_git_url

Magic Castle configuration management is handled by
[Puppet](https://en.wikipedia.org/wiki/Puppet_(software)). The Puppet
configuration files are stored in a git repository. This is
typically [ComputeCanada/puppet-magic_castle](https://www.github.com/ComputeCanada/puppet-magic_castle) repository on GitHub.

Leave this variable to its current value for this tutorial.

## config_version

Since Magic Cluster configuration is managed with git, it is possible to specify
which version of the configuration you wish to use. Typically, it will match the
version number of the release you have downloaded (i.e: `9.3`).

Leave this variable to its current value for this tutorial.

## cluster_name

This variable defines the name of your cluster. Choose an original name for your cluster. Limit yourself to alphanumeric characters and dashes.

## image

This variable defines the name of the image that will be used as the 
base image for the cluster nodes. The operating system on the image 
must be from the RedHat family. This includes CentOS (7, 8), 
Rocky Linux (8), and AlmaLinux (8).

Leave this variable to its current value for this tutorial.

## 