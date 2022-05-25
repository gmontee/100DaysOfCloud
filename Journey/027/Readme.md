<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/YN6qUXj4HdXoY/giphy.gif" width="500"/>
</div>

# Day 27 - Azure AZ-204 Monitor services that are deployed to Azure

## Introduction

☁️ Today, I'm going to configure and test Application Insights logging of an web API app

## Prerequisite

☁️ Application Insights monitors Azure services for availability, performance, failures, and usage by combining data from Application Insights SDKs with Azure Diagnostics data from your cloud services

## Use Case

<div id="use case" align="center">
  <img src="https://microsoftlearning.github.io/AZ-204-DevelopingSolutionsforMicrosoftAzure/Instructions/Labs/media/Lab11-Diagram.png" width="600"/>
</div>

- Troubleshoot solutions by using metrics and log data
  - **configure an app or service to use Application Insights**
  - review and analyze metrics and log data
  - implement Application Insights web tests and alerts

## Cloud Research

☁️ Application Insights is a feature of Azure Monitor

- Application Insights provides:
  - automatically detect performance issues
  - help diagnose issues
  - see what users are actually doing in the app
  - help continuously improve app performance and usability

☁️ Telemetry: the automatic measurement and wireless transmission of data from remote sources

## My Experience

### Step 0 — Create Prerequisite Resources

Create an Application Insights resource

<div align="center">
  <img src="images/az204-insightlab-task0-create-app-insights.png" width="800"/>
  <img src="images/az204-insightlab-task0-create-app-insights1.png" width="800"/>
</div>

### Task 1 — Create an Azure Web API resource

Create an Azure Web API resource

<div align="center">
  <img src="images/az204-insightlab-task1-create-web-app.png" width="800"/>
  <img src="images/az204-insightlab-task1-create-web-app1.png" width="800"/>
  <img src="images/az204-insightlab-task1-create-web-app2.png" width="800"/>
</div>

Configure web API autoscale options

<div align="center">
  <img src="images/az204-insightlab-task1-auto-scale.png" width="800"/>
  <img src="images/az204-insightlab-task1-auto-scale1.png" width="800"/>
</div>

### Task 2 — Monitor a local web API by using Application Insights

Build a .NET Web API project

<div align="center">
  <img src="images/az204-insightlab-task2-dotnet-app.png" width="800"/>
  <img src="images/az204-insightlab-task2-dotnet-app1.png" width="800"/>
  <img src="images/az204-insightlab-task2-dotnet-app2.png" width="800"/>
  <img src="images/az204-insightlab-task2-dotnet-app3.png" width="800"/>
</div>

Update app code to disable HTTPS and use Application Insights

<div align="center">
  <img src="images/az204-insightlab-task2-app-code.png" width="800"/>
</div>

Test an API application locally

<div align="center">
  <img src="images/az204-insightlab-task2-local-test.png" width="800"/>
  <img src="images/az204-insightlab-task2-local-test1.png" width="800"/>
</div>

Review metrics in Application Insights

<div align="center">
  <img src="images/az204-insightlab-task2-review-metrics.png" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ Obviously, just scratching the mere surface of what is possible with Application Insights

## Next Steps

Tomorrow, I'm going to learn about utilize Azure Content Delivery Network

## Social Proof

[Linkedin Post](https://www.linkedin.com/posts/georgemontee_github-gmontee100daysofcloud-activity-6935235821570519041-NoiN?utm_source=linkedin_share&utm_medium=member_desktop_web)
