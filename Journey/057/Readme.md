<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/8ENiS6ejIUlvK16Jwp/giphy.gif" width="500"/>
</div>

# Day 57 - Terraform - Providers

## Introduction

☁️ Today I'm going to learn about Providers in Terraform

## Prerequisite

☁️ Terraform uses plugins referred to as "providers" to interact with cloud providers, Service-as-a-Service providers, and other API's.

## Use Case

<div id="use case" align="center">
  <img src="https://www.datocms-assets.com/2885/1653430998-verified-blog-visual-3.png?fit=max&fm=png&q=80" width="600"/>
</div>

As of the writing of this post, there are a combined 251 Official and Verified Providers for Terraform. Official providers are owned and maintained by HashiCorp, while the Verified is owned and mantained by 3rd-party tech partners, e.g., auth0, F5 bigip, Cloudflare, VMWare nsxt, splunk, etc.

## Cloud Research

☁️ Terraform modules must declare which providers it requires via `required_providers` block, which includes local name, source location, and version contraint

☁️ Local names are module-specific, and must be unique per module; each Provider has a preferred local name, e.g., aws, azurerm, google

☁️ Source Addresses is it's global identifier, e.g., registry.terraform.io/hashicorp/http

☁️ Version Contraints is optional, although highly recommended to ensure functionality doesn't break unexpectantly with new versions

## My Experience

### Task 1 — Summary of Step

<div align="center">
  <img src="images/" width="800"/>
</div>

### Task 2 — Summary of Step

<div align="center">
  <img src="images/" width="800"/>
</div>

### Task 3 — Summary of Step

<div align="center">
  <img src="images/" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ Doing some research, one can develop their Terraform provider [calling HashiCorp's API](https://learn.hashicorp.com/collections/terraform/providers); can still use them without publishing them on the public Terraform Registry

## Next Steps

☁️ Tomorrow, I'm going to learn about leveraging variables in Terraform

## Social Proof

[Linkedin Post]()
