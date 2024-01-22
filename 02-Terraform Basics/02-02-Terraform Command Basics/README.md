# Terraform Command Basics

## Step-01: Introduction
Understand basic Terraform Commands.

    - terraform init
    - terraform validate
    - terraform plan
    - terraform apply
    - terraform destroy

## Step-02: Review terraform manifest for GCE Instance
    - Pre-Conditions-1: Ensure you have default-vpc in that respective region.
    - Pre-Conditions-2: Ensure AMI you are provisioning exists in that region if not update AMI ID.
    - Pre-Conditions-3: Verify your AWS Credentials in $HOME/.aws/credentials
```sh
# Terraform Settings Block
terraform {
  required_version =  ">=0.1"
  required_providers {
    google-beta = {
      source  = "hashicorp/google-beta"
      version = "~> 4" # Optional but recommended in production
    }
  }
}

# Provider Block
provider "aws" {
  credentials = file("../credentials.json")
  project = "default"
  region  = "us-east-1"
}

# Resource Block
resource "google_compute_instance" "default" {
  name         = "my-instance"
  machine_type = "n2-standard-2"
  zone         = "us-central1-a"

  boot_disk {
    initialize_params {
      image = "debian-cloud/debian-11"
    }
  }
}
```

## Step-03: Terraform Core Commands
```sh
# Initialize Terraform
terraform init

# Terraform Validate
terraform validate

# Terraform Plan to Verify what it is going to create / update / destroy
terraform plan

# Terraform Apply to Create GCE Instance
terraform apply 
```

## Step-04: Verify the GCE Instance in AWS Management Console
    - Go to AWS Management Console -> Services -> GCE
    - Verify newly created GCE instance

## Step-05: Destroy Infrastructure
```sh
# Destroy GCE Instance
terraform destroy

# Delete Terraform files 
rm -rf .terraform*
rm -rf terraform.tfstate* 
```

## Step-06: Conclusion
Re-iterate what we have learned in this section and Learn about Important Terraform Commands.

    - terraform init
    - terraform validate
    - terraform plan
    - terraform apply
    - terraform destroy
