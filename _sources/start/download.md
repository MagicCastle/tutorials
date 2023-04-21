# Download Magic Castle

1. Go to https://github.com/ComputeCanada/magic_castle/releases.
2. Download the latest zip release of Magic Castle for your cloud provider.
3. Open a Terminal.
4. Uncompress the release: `unzip magic_castle*.zip`
5. Rename the release folder after your favourite superhero: `mv magic_castle* hulk`
6. Move inside the folder: `cd hulk`

The file `main.tf` contains Terraform modules and outputs. Modules are files that define a set of
resources that will be configured based on the inputs provided in the module block.
Outputs are used to tell Terraform which variables of
our module we would like to be shown on the screen once the resources have been instantiated.

This file will be our main canvas to design our new clusters. As long as the module block
parameters suffice to our need, we will be able to limit our configuration to this sole
file. Further customization will be addressed during the second part of the tutorial.

