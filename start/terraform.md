# Terraform

Magic Castle uses the open-source software Terraform and HashiCorp Language (HCL) to define the virtual machines, volumes, and networks that are required to replicate a virtual HPC infrastructure. The infrastructure definition is packaged as a Terraform module that users can customize as they require.

To install Terraform, follow the
[tutorial](https://learn.hashicorp.com/tutorials/terraform/install-cli)
or go directly on [Terraform download page](https://www.terraform.io/downloads).

You can verify Terraform was properly installed by looking at the version in a terminal:
```
terraform version
```
