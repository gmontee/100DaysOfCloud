<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/l0G17R0PwQRo0PFrG/giphy.gif" width="300"/>
</div>

# Day 60 - Terraform - Storing State Remotely

## Introduction

☁️ Today I'm going to learn about storing Terraform state remotely

## Prerequisite

☁️ As previously mentioned, Terraform state allows Terraform to track deployed resources, allowing it to know what to add, update, and/or delete

## Use Case

☁️ Working in a collaborative environment, or leveraging a CI/CD pipeline, saving Terraform state locally doesn't work from a practical standpoint

## Cloud Research

One possible solution is to store the state file with a Cloud Provider. In today's example, I'm going to store the state file on Azure. To do this I need the following:

- A Resource Group
- A Storage Account
- A Blob Container

In future Terraform usage, I can reference that cloud stored state file.

## My Experience

### Task 1 — Writing the Terraform Code

I created a separate Providers file to keep things cleaner

<div align="center">
  <img src="images/terraform-task1-provider.jpg" width="800"/>
</div>

Here I'm creating those three things mentioned earlier need to save the state file remotely.

<div align="center">
  <img src="images/terraform-task1-create-storage.jpg" width="800"/>
</div>

### Task 2 — Creating the Storage resources

Initializing the providers

<div align="center">
  <img src="images/terraform-task2-terraform-init.jpg" width="800"/>
</div>

I know this is long, but wanted to highlight that from a few declarative Terraform commands working with the Azure Resource Manager API, all this resources and attributes are going to be generated

<div align="center">
  <img src="images/terraform-task2-plan1.jpg" width="800"/>
  <img src="images/terraform-task2-plan2.jpg" width="800"/>
  <img src="images/terraform-task2-plan3.jpg" width="800"/>
  <img src="images/terraform-task2-plan4.jpg" width="800"/>
</div>

Applying...

<div align="center">
  <img src="images/terraform-task2-apply.jpg" width="800"/>
</div>

Here is the new container in Azure

<div align="center">
  <img src="images/terraform-task2-azure.jpg" width="800"/>
</div>

### Step 3 — Leveraging the Remote State

First I need to export the access key for the storage account to an environment variable

`ACCOUNT_KEY=$(az storage account keys list --resource-group 'tfstate' --account-name 'tfstate5qjhq' --query '[0].value' -o tsv)`

`export ARM_ACCESS_KEY=$ACCOUNT_KEY`

I've created another Terraform project. This time I incorporate the backend block in my providers file

<div align="center">
  <img src="images/terraform-task3-backend.jpg" width="800"/>
</div>

I know it's boring, but I'm just going to create a resource group to demonstrate using a remote state file

<div align="center">
  <img src="images/terraform-task3-rg.jpg" width="800"/>
</div>

When I run my terraform commands, no state files are created locally

<div align="center">
  <img src="images/terraform-task3-nolocal.jpg" width="800"/>
</div>

The tfstate container now has a file name terraform.tfstate. Since I have a plan command in use, notice at the bottom the Lease Status is "Locked". Since my code is utilizing the state file, the blob is leased preventing others from modifying or deleting it.

<div align="center">
  <img src="images/terraform-task3-lease.jpg" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ Being straight forward to setup a storage account for the state file, a way to reference and access it, and maintain state regardless of your location. I can see this being crucial in a CI/CD setup where the agents are drawn from a pool, and discarded after use.

## Next Steps

☁️ Tomorrow, I'm going to learn about Data Sources in Terraform

## Social Proof

[Linkedin Post]()
