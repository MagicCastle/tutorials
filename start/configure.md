# Configure your cluster

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

## config_git_url

Magic Castle configuration management is handled by
[Puppet](https://en.wikipedia.org/wiki/Puppet_(software)). The Puppet
configuration files are stored in a git repository. This is
typically [ComputeCanada/puppet-magic_castle](https://www.github.com/ComputeCanada/puppet-magic_castle) repository on GitHub.

We will leave this variable to its current value for this tutorial.

## config_version

Since Magic Cluster configuration is managed with git, it is possible to specify
which version of the configuration you wish to use. Typically, it will match the
version number of the release you have downloaded (i.e: `9.3`).

We will leave this variable to its current value for this tutorial.

## cluster_name

This variable defines the name of your cluster. It must be lowercase alphanumeric characters and start with a letter and can include dashes. `cluster_name` must be 63 characters or less.

Change this variable to match the name of your folder.


