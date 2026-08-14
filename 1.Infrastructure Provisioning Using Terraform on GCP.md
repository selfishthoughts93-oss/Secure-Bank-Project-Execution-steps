# Stage 1: Infrastructure Provisioning Using Terraform on GCP

## Objective

Provision the required Virtual Machines and Networking Components on Google Cloud Platform using Terraform and Visual Studio Code.

---

## Prerequisites

- Google Cloud Platform Account
- GCP Project Created
- Terraform Installed
- Google Cloud SDK Installed
- Visual Studio Code Installed
- Service Account Key (JSON)

---

## Project Files

```text
provider.tf
variables.tf
versions.tf
network.tf
firewall.tf
vm.tf
terraform.tfvars
```

---

## Configure GCP Authentication

```bash
gcloud auth login
```

```bash
gcloud config set project <PROJECT_ID>
```

---

## Verify Terraform Installation

```bash
terraform version
```

---

## Initialize Terraform

```bash
terraform init
```

---

## Validate Terraform Configuration

```bash
terraform validate
```

---

## Format Terraform Files

```bash
terraform fmt
```

---

## Review Infrastructure Plan

```bash
terraform plan
```

---

## Create Infrastructure

```bash
terraform apply
```

Type:

```text
yes
```

Or

```bash
terraform apply -auto-approve
```

---

## Verify Resources

### List Virtual Machines

```bash
gcloud compute instances list
```

### List Networks

```bash
gcloud compute networks list
```

### List Subnets

```bash
gcloud compute networks subnets list
```

### List Firewall Rules

```bash
gcloud compute firewall-rules list
```

---

## Connect to Virtual Machines

### Jenkins VM

```bash
gcloud compute ssh <jenkins-vm-name> --zone asia-south1-c
```

### Docker VM

```bash
gcloud compute ssh <docker-vm-name> --zone asia-south1-c
```

### SonarQube VM

```bash
gcloud compute ssh <sonarqube-vm-name> --zone asia-south1-c
```

### Monitoring VM

```bash
gcloud compute ssh <monitoring-vm-name> --zone asia-south1-c
```

---

## Check Terraform State

```bash
terraform state list
```

---

## Destroy Infrastructure

```bash
terraform destroy
```

Or

```bash
terraform destroy -auto-approve
```

---

## Outcome

Successfully provisioned:

- VPC Network
- Subnet
- Firewall Rules
- Jenkins VM
- Docker VM
- SonarQube VM
- Monitoring VM

using Terraform on Google Cloud Platform.
