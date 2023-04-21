# Configure cloud credentials

For Terraform to be able to communicate with the cloud provider API, it needs access to your
credentials.

Each cloud provider has its own procedure.

## Amazon Web Services (AWS)
<!-- markdown-link-check-disable -->
1. Go to [AWS - My Security Credentials](https://console.aws.amazon.com/iam/home?#/security_credentials)
2. Create a new access key.
3. In a terminal, export `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`, environment variables, representing your AWS Access Key and AWS Secret Key:
    ```shell
    export AWS_ACCESS_KEY_ID="an-access-key"
    export AWS_SECRET_ACCESS_KEY="a-secret-key"
    ```
<!-- markdown-link-check-enable -->

## Google Cloud

1. Install the [Google Cloud SDK](https://cloud.google.com/sdk/docs/downloads-interactive)
2. In a terminal, enter :
    ```
    gcloud auth application-default login
    ```

## Microsoft Azure

1. Install [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli)
2. In a terminal, enter : 
    ```
    az login
    ```

## Jetstreams 2 / OpenStack / OVH

1. Download your OpenStack Open RC file.
It is project-specific and contains the credentials used
by Terraform to communicate with OpenStack API.
To download, using OpenStack web page go to:
**Project** → **API Access**, then click on **Download OpenStack RC File**
then right-click on **OpenStack RC File (Identity API v3)**, **Save Link as...**,
and save the file.

2. In a terminal located in the same folder as your OpenStack RC file,
source the OpenStack RC file:
    ```
    source *-openrc.sh
    ```
This command will ask for a password, enter your OpenStack password.