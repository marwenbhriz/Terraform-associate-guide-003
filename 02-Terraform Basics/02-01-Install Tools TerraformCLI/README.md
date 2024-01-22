# Terraform and GCloud CLI Installation

## Step-01: Introduction
    - Install Terraform CLI.
    - Install GCloud CLI.
    - Install VS Code Editor.
    - Install HashiCorp Terraform plugin for VS Code.

## Step-02: Terraform Install
01. Download [Terraform](https://developer.hashicorp.com/terraform/install). 
02. Install [CLI](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli).
03. Install HashiCorp Terraform plugin for VS Code.

```sh
# Copy binary zip file to a folder
mkdir /Users/<YOUR-USER>/Documents/terraform-install
COPY Package to "terraform-install" folder

# Unzip
unzip <PACKAGE-NAME>
unzip terraform_0.14.3_darwin_amd64.zip

# Copy terraform binary to /usr/local/bin
echo $PATH
mv terraform /usr/local/bin

# Verify Version
terraform version

# To Uninstall Terraform (NOT REQUIRED)
rm -rf /usr/local/bin/terraform
```

## Step-03: MACOS: IDE for Terraform - VS Code Editor
01. Download [Microsoft Visual Studio Code Editor](https://code.visualstudio.com/download). 
02. Install [Hashicorp Terraform Plugin for VS Code](https://marketplace.visualstudio.com/items?itemName=HashiCorp.terraform).

## Step-04: MACOS: Install GCLOUD CLI
01. Download [GCloud CLI](https://cloud.google.com/sdk/docs/install?hl=fr#mac). 
02. Install [GCloud CLI](https://cloud.google.com/sdk/docs/install?hl=fr#mac).
```sh
# Install gcloud cli
./google-cloud-sdk/install.sh
```

## Step-05: MACOS: Configure AWS Credentials
```sh
# gcloud login and then open the link from browser and copy/past the code received after authentication
gcloud auth login

# gcloud set account/project
export ACCOUNT_ID=
export PROJECT_ID=
gcloud config set account $ACCOUNT_ID
gcloud config set project $PROJECT_ID
```