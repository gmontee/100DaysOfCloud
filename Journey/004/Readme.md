<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/81xwEHX23zhvy/giphy.gif" width="500"/>
</div>

# Day 4 - Azure AZ-104 Manage Governance via Azure Policy Lab

## Introduction

Yesterday, I walked through Lab 2a, Manage Subscriptions and RBAC, from [Microsoft Learn AZ-104 Lab Exercises](https://microsoftlearning.github.io/AZ-104-MicrosoftAzureAdministrator/). Today, I'm doing Lab 2b, Manage Governance via Azure Policy Lab.

## Prerequisite

[Azure Policies](https://docs.microsoft.com/en-us/azure/governance/policy/overview) are used to enforce business rules on resources. It could be ensuring naming conventions are followed, only certain virtual machine SKUs resources are created in a particular region, restrict access to an Azure service, requiring tagging, etc.

## Use Case

<div id="cover photo" align="center">
  <img src="https://microsoftlearning.github.io/AZ-104-MicrosoftAzureAdministrator/Instructions/media/lab02b.png" width="600"/>
</div>

- This architecture diagram is taken from the lab page, showing the three tasks:
  - Task 1: Create and assign tags via the Azure portal
  - Task 2: Enforce tagging via an Azure policy
  - Task 3: Apply tagging via an Azure policy

## Try yourself

### Step 1 — Create and assign tags via the Azure portal

Here's I'm showing the tag Role:Infra is in place

<div align="center">
  <img src="images/az104-lab3-task1-tag-storage.png" width="800"/>
</div>

### Step 2 — Enforce tagging via an Azure policy

Filtering to policy definitions related to tags.

<div align="center">
  <img src="images/az104-lab3-task2-definition-tag.png" width="800"/>
</div>

Creating the policy

<div align="center">
  <img src="images/az104-lab3-task2-create-policy.png" width="800"/>
</div>

Here the attempt to deploy a new storage account without the necessary tag fails validation

<div align="center">
  <img src="images/az104-lab3-task2-deploy-storage.png" width="800"/>
</div>

### Step 3 — Apply tagging via an Azure policy

Creating the policy for resources to inherit a certain tag from the resource group

<div align="center">
  <img src="images/az104-lab3-task3-inherit-policy.png" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ Yesterday, working with RBAC, that was for controlling user actions at different scopes. Policy, however, maintains compliance with resources.

☁️ Applying and removing policies isn't instant, so you might have to wait 5-15 minutes.

☁️ Previously, I had used the Portal, Azure CLI, and PowerShell to apply, to modify, and remove tags. Applying tags via Policy sounds extremely useful.

☁️ I'm not sure why, yet, but sometimes the Azure Portal will attempt to create resources in a different region. It's kind of annoying for consistency

## Next Steps

Tomorrow, I'm going to do the fourth lab, [3a Manage Azure resources by Using the Azure Portal](../005/Readme.md), from the Azure Administration module.

## Social Proof

[Linkedin Post](https://www.linkedin.com/posts/georgemontee_github-gmontee100daysofcloud-activity-6920364586839752704-oLHG?utm_source=linkedin_share&utm_medium=member_desktop_web)
