<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/orVyU8bAWlNfE0i021/giphy.gif" width="500"/>
</div>

# Day 14 - Azure AZ-204 Configure Web App Settings

## Introduction

☁️ Yesterday's lab I created a static HTML web app by using Azure Cloud Shell. Today, I'm going to dig deeper into Azure App Service by looking at application settings, installing SSL/TLS certificates to secure web traffic, enable diagnostic logging, creating virtual app to directory mappings, and managing app features.

## Prerequisite

☁️ The Azure App Service is a HTTP-based service for hosting web applications, REST APIs, and mobile back ends.

## Use Case

<div id="use case" align="center">
  <img src="https://aspblogs.blob.core.windows.net/media/scottgu/WindowsLiveWriter/AnnouncingthenewAzureAppService_122D1/image_4.png" width="600"/>
</div>

## Cloud Research

- ☁️ Configure App Settings
- App's Management page --> Configuration --> Application Settings
- App settings are variables passed as environment variables to the application code
- For Linux and custom containers use the --env flag
- For ASP.NET and ASP.NET Core, <appSettings> in the Web.config
- App settings are always encrypted when stored (encrypted-at-rest)

<div align="center">
  <img src="https://docs.microsoft.com/en-us/learn/wwl-azure/configure-web-app-settings/media/configure-app-settings.png" width="800"/>
</div>

☁️ General Settings

App's Management page --> Configuration --> General Settings
Stack Settings: software stack to run the app, language, and SDK versions

Platform Settings:

- 32 or 64 bit
- WebSocket Protocol
- Always On: keeps the app loaded
- Managed pipeline version: for IIS
- HTTP version
- ARR affinity: off for stateless, on for client to route to same instance during session
- Debugging
- Incoming client certificates: mutual authentication

☁️ Configure path mappings

- Windows

  - IIS handler mappings
  - Extension
  - Script processor
  - Arguments

- Linux (and containerized apps)

  - Name
  - Config options: basic or advanced
  - Storage Accounts: Azure Blobs or Azure Files
  - Storage Type
  - Share Name
  - Access key
  - Mount path

☁️ Enable diagnostic logging

- Windows or Linux

  - Application logging
  - Deployment logging

- Windows only

  - Web server logging
  - Detailed error logging
  - Failed request tracing

☁️ Configure Security Certificates

- Create a free App Service managed certificate
- Purchase an App Service certificate
- Import a certificate from Key Vault
- Upload a private certificate
- Upload a public certificate

☁️ Manage App Features

- Feature Flag: variable with binary on/off state
- Feature Manager: application package that handles the lifecycle of all the feature flags in an app
- Filter: rule for evaluating state of feature flag

## Next Steps

☁️ Tomorrow, I'm going to look at scaling apps in the Azure App Service

## Social Proof

[Linkedin Post]()
