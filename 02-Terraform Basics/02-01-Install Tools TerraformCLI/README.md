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

## Step-01: Introduction

## Step-01: Introduction
