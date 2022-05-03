<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/BNfSvT4oflVIQfwHWj/giphy.gif" width="500"/>
</div>

# Day 12 - Azure AZ-204 Azure App Service

## Introduction

☁️ Yesterday's lab was focused on creating a unified mesh topology. Today, I'm learning about the Azure App Service via the Microsoft Learn 'Explore Azure App Service' module.

## Prerequisite

☁️ The Azure App Service is a HTTP-based service for hosting web applications, REST APIs, and mobile back ends.

## Use Case

<div id="use case" align="center">
  <img src="https://aspblogs.blob.core.windows.net/media/scottgu/WindowsLiveWriter/AnnouncingthenewAzureAppService_122D1/image_4.png" width="600"/>
</div>

## Cloud Research

- ☁️ Auto Scaling

  - Up/Down: changing the number of cores or the amount of memory
  - Out/In: changing the number of machine instances running

- ☁️ Continuous Integration & Deployment

  - Azure DevOps
  - GitHub
  - Bitbucket
  - FTP
  - Local Git repo on a dev machine

- ☁️ Deployment Slots (Standard or Premium plan tiers)

  - Slots can be used for staging and production builds. Slots can be swapped, aka Blue/Green deployment.

- ☁️ Supports multiple languages and frameworks

  - Can't mix Windows and Linux apps in the same App Service plan
  - Hosted on Windows or Linux
    - ASP.NET Core
    - PHP
    - Node.js
    - Java
    - HTML
  - Windows Only
    - ASP.NET
  - Linux Only
    - Ruby
    - Python

- ☁️ App Service Plans

  - defines a set of compute resources for a web app to run
  - One or more apps can run on the same compute resources
  - Azure Functions can be ran
  - are the scale unit

- ☁️ App Service plan contains:

  - Region
  - Number of VM instances
  - Size of VM instances (Small, Medium, Large)
  - Pricing tier

- ☁️ App Service Pricing Tiers

  - Shared: dev/test, can't scale out, shared with other customers
    - Free
    - Shared
  - Dedicated: only apps in same service plan share resources, higher tiers equal more vm instances for scaling out
    - Basic
    - Standard
    - Premium
    - PremiumV2
    - PremiumV3
  - Isolated: runs on dedicated VNet, maximum scale-out capability
  - Consumption: function apps, scales dynamically depending on workload

- ☁️ Automated Deployment

  - process used to push out new features and bug fixes in a fast and repetitive pattern with minimal impact on end users
    - Azure DevOps
    - GitHub
    - Bitbucket

- ☁️ Manual Deployment

  - manually push your code to Azure
    - Git
    - CLI
    - Zip deploy
    - FTP/S

- ☁️ Built-in Authentication

  - out-of-the-box authentication with federated identity providers
  - can integrate with multiple login providers
  - authentication and authorization module runs in the same sandbox as your app code
    - Authenticates users with the specified token
    - Validates, stores, and refreshes tokens
    - Manages the authenticated session
    - Injects identity information into request headers

- ☁️ Identity Providers

  - Microsoft Identify Platform
  - Facebook
  - Google
  - Twitter
  - Any OpenID Connect provider

- ☁️ Authentication Flow

  - Without provider SDK (server-directed flow): browser apps
  - WIth provider SDK (client-directed flow): REST APIs, Azure Functions, JavaScript browser clients, native mobile apps

- ☁️ Authorization Behavior

  - Allow unauthenticated requests - defers to app code
  - Require authentications

- ☁️ Multi-tenant App Service networking features
  - Front ends: role that handle incoming HTTP/S requests
  - Workers: roles that host the customer workload
  - Inbound Features
    - App-assigned address
    - Access restrictions
    - Service endpoints
    - Private endpoints
  - Outbound Features
    - Hybrid Connections
    - Gateway-required virtual network integration
    - Virtual network integration

## ☁️ Cloud Outcome

☁️ That was a lot to take in. I need to review this content using [John Savill's video](https://youtu.be/_E73_SQN8ZU?t=4875), or this portion of the [A Cloud Guru course](https://learn.acloud.guru/course/az-204-developing-solutions-for-microsoft-azure/overview).

## Next Steps

☁️ Tomorrow, I'm going to create a static HTML web app by using Azure Cloud Shell

## Social Proof

[Linkedin Post]()
