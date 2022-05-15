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

☁️

## My Experience

### Step 0 — Create Prerequisite Resources

Creating the storage account

<div align="center">
  <img src="images/" width="800"/>
</div>

Grabbing the access keys

<div align="center">
  <img src="images/" width="800"/>
</div>

Creating the Azure Key Vault

<div align="center">
  <img src="images/" width="800"/>
</div>

Creating a Function app

<div align="center">
  <img src="images/" width="800"/>
</div>

### Task 1 — Configure secrets and identities

Configure a system-assigned managed service identity

<div align="center">
  <img src="images/" width="800"/>
</div>

Create a Key Vault secret

<div align="center">
  <img src="images/" width="800"/>
</div>

Configure a Key Vault access policy

<div align="center">
  <img src="images/" width="800"/>
</div>

Create a Key Vault-derived application setting

<div align="center">
  <img src="images/" width="800"/>
</div>

### Task 2 — Build an Azure Functions app

Initialize a function project

<div align="center">
  <img src="images/" width="800"/>
</div>

Create an HTTP-triggered function

<div align="center">
  <img src="images/" width="800"/>
</div>

Configure and read an application setting

<div align="center">
  <img src="images/" width="800"/>
</div>

Validate the local function

<div align="center">
  <img src="images/" width="800"/>
</div>

Deploy the function using the Azure Functions Core Tools

<div align="center">
  <img src="images/" width="800"/>
</div>

Test the Key Vault-derived application setting

<div align="center">
  <img src="images/" width="800"/>
</div>

### Task 3 — Access Azure Blob Storage data

Upload a sample storage blob

<div align="center">
  <img src="images/" width="800"/>
</div>

Pull and configure the Azure SDK for .NET

<div align="center">
  <img src="images/" width="800"/>
</div>

Deploy and validate the Azure Functions app

<div align="center">
  <img src="images/" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️

## Next Steps

Tomorrow, I'm going to learn about

## Social Proof

[Linkedin Post]()
