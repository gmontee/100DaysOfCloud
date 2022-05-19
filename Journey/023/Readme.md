<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/CCdZOITMQoSIrRs283/giphy.gif" width="500"/>
</div>

# Day 23 - Azure AZ-204 Access resource secrets more securely across services

## Introduction

☁️ Today, I'm going to use an Azure Function app utilizing C# code to access a storage account, and then download the contents

## Prerequisite

☁️ Azure Key Vault a cloud service for securely storing and accessing secrets

## Use Case

<div id="use case" align="center">
  <img src="https://microsoftlearning.github.io/AZ-204-DevelopingSolutionsforMicrosoftAzure/Instructions/Labs/media/Lab07-Diagram.png" width="600"/>
</div>

- Implement Secure Cloud Solutions
  - secure app configuration data by using App Configuration or Azure Key Vault
  - develop code that uses keys, secrets, and certificates stored in Azure Key Vault
  - implement Managed Identities for Azure resources

## Cloud Research

- Secret - anything you want to tightly control access to
  - API Keys
  - Passwords
  - Certificates
  - Cryptographic Keys

## My Experience

### Step 0 — Create Prerequisite Resources

Creating the storage account

<div align="center">
  <img src="images/az204-seclab-task0-storage-account.png" width="800"/>
</div>

Grabbing the access keys

<div align="center">
  <img src="images/az204-seclab-task0-access-keys.png" width="800"/>
</div>

Creating the Azure Key Vault

<div align="center">
  <img src="images/az204-seclab-task0-create-vault.png" width="800"/>
</div>

Creating a Function app

<div align="center">
  <img src="images/az204-seclab-task0-create-func1.png" width="800"/>
  <img src="images/az204-seclab-task0-create-func2.png" width="800"/>
</div>

### Task 1 — Configure secrets and identities

Configure a system-assigned managed service identity

<div align="center">
  <img src="images/az204-seclab-task1-system-identity.png" width="800"/>
  <img src="images/az204-seclab-task1-system-identity1.png" width="800"/>
</div>

Create a Key Vault secret

<div align="center">
  <img src="images/az204-seclab-task1-generate-keys.png" width="800"/>
  <img src="images/az204-seclab-task1-generate-keys1.png" width="800"/>
</div>

Configure a Key Vault access policy

<div align="center">
  <img src="images/az204-seclab-task1-add-policy.png" width="800"/>
  <img src="images/az204-seclab-task1-add-policy1.png" width="800"/>
  <img src="images/az204-seclab-task1-add-policy2.png" width="800"/>
  <img src="images/az204-seclab-task1-add-policy3.png" width="800"/>
</div>

Create a Key Vault-derived application setting

<div align="center">
  <img src="images/az204-seclab-task1-app-key.png" width="800"/>
  <img src="images/az204-seclab-task1-app-key1.png" width="800"/>
</div>

### Task 2 — Build an Azure Functions app

Initialize a function project

<div align="center">
  <img src="images/az204-seclab-task2-initialize-app.png" width="800"/>
</div>

Create an HTTP-triggered function

<div align="center">
  <img src="images/az204-seclab-task2-initialize-app1.png" width="800"/>
</div>

Configure and read an application setting

<div align="center">
  <img src="images/az204-seclab-task2-app-setting.png" width="800"/>
  <img src="images/az204-seclab-task2-app-setting1.png" width="800"/>
</div>

Validate the local function

<div align="center">
  <img src="images/az204-seclab-task2-validate-func.png" width="800"/>
  <img src="images/az204-seclab-task2-validate-func1.png" width="800"/>
</div>

Deploy the function using the Azure Functions Core Tools

<div align="center">
  <img src="images/az204-seclab-task2-deploy-func.png" width="800"/>
</div>

Test the Key Vault-derived application setting

<div align="center">
  <img src="images/az204-seclab-task2-test-func.png" width="800"/>
  <img src="images/az204-seclab-task2-test-func1.png" width="800"/>
  <img src="images/az204-seclab-task2-test-func2.png" width="800"/>
  <img src="images/az204-seclab-task2-test-func3.png" width="800"/>
</div>

### Task 3 — Access Azure Blob Storage data

Upload a sample storage blob

<div align="center">
  <img src="images/az204-seclab-task3-storage-blob.png" width="800"/>
  <img src="images/az204-seclab-task3-storage-blob1.png" width="800"/>
  <img src="images/az204-seclab-task3-storage-blob2.png" width="800"/>
  <img src="images/az204-seclab-task3-storage-blob3.png" width="800"/>
  <img src="images/az204-seclab-task3-storage-blob4.png" width="800"/>
</div>

Pull and configure the Azure SDK for .NET

<div align="center">
  <img src="images/az204-seclab-task3-azure-sdk.png" width="800"/>
  <img src="images/az204-seclab-task3-azure-sdk1.png" width="800"/>
</div>

Deploy and validate the Azure Functions app

<div align="center">
  <img src="images/az204-seclab-task4-validate-func.png" width="800"/>
  <img src="images/az204-seclab-task4-validate-func1.png" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ So close, yet, I'm met with failure again! I created an ARM template and parameters of the resource group and it's resources, and then deleted the rg. I came back to it later, using the ARM files to deploy the resources again. Unfortunately, the deployment failed, saying anomalies detected.

☁️ Yesterday, I believe the friction was between .NET Core 3.1 and .NET 6; the lab was originally created with the former, but I had .NET 6 installed for other labs and projects. For today, one area I might've goofed, was copying or inputting quotation marks in regards to the secret.

☁️ Alright, I've hit a few bumps. Obviously, doesn't feel great, but I need to keep trucking on. I have a week left until the exam.

## Next Steps

Tomorrow, I'm going to learn about creating a multi-tier solution using Azure services.

## Social Proof

[Linkedin Post](https://www.linkedin.com/posts/georgemontee_github-gmontee100daysofcloud-activity-6933047799831826432-peSV?utm_source=linkedin_share&utm_medium=member_desktop_web)
