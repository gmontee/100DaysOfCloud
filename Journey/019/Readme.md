<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/uurtMtTKqkJda4dk8Y/giphy-downsized-large.gif" width="500"/>
</div>

# Day 19 - Azure AZ-204 Implement Azure Functions

## Introduction

☁️ Azure functions is a serverless concept of cloud native design that allows a piece of code deployed and execute without any need of server infrastructure, web server, or any configurations

## Prerequisite

☁️ Serverless Computing is a method of providing backend services on an as-used basis

## Use Case

<div id="use case" align="center">
  <img src="https://microsoftlearning.github.io/AZ-204-DevelopingSolutionsforMicrosoftAzure/Instructions/Labs/media/Lab02-Diagram.png" width="600"/>
</div>

- Implement Azure functions:
  - **Create and deploy Azure Functions app**
  - Implement input and output bindings to a function
  - Implement function triggers by using data operations, timers, and webhooks
  - Implement Azure Durable Functions
  - Implement custom handlers

## Cloud Research

☁️ Azure functions are lightweight, serverless, easier to write and deploy

☁️ Azure functions can be written in multiple languages: C#, Java, JavaScript, TypeScript, Python

☁️ Azure functions are scalable; resources are allocated/unallocated based on demand

☁️ Azure functions execution is triggered when an event is fired

☁️ Azure functions can be built, tested, and deployed in the Azure Portal

## My Experience with Azure Functions

### Task 0 — Configure Local Environment

I need to download and install the .NET SDK and Runtime on my Ubuntu 21.10 box.

Adding the Microsoft package signing key to my list of trusted keys, and adding the package repo.

<div align="center">
  <img src="images/az204-functionlab-task0-mspackage.png" width="800"/>
  <img src="images/az204-functionlab-task0-package-repo.png" width="800"/>
</div>

Installing the .NET SDK locally

<div align="center">
  <img src="images/az204-functionlab-task0-dotnet-sdk1.png" width="800"/>
  <img src="images/az204-functionlab-task0-dotnet-sdk2.png" width="800"/>
  <img src="images/az204-functionlab-task0-dotnet-sdk3.png" width="800"/>
</div>

Installing the Azure Functions Core Tools locally

<div align="center">
  <img src="images/az204-functionlab-task0-func-core-tools.png" width="800"/>
</div>

Installing the Azure CLI locally

<div align="center">
  <img src="images/az204-functionlab-task0-azurecli1.png" width="800"/>
</div>

Double-checking versions installed

<div align="center">
  <img src="images/az204-functionlab-task0-versions.png" width="800"/>
</div>

### Task 1 — Create a local Function project

Creating the Function project and the HttpExample function on my local machine

<div align="center">
  <img src="images/az204-functionlab-task1-create-func-proj.png" width="800"/>
</div>

### Task 2 — The Function itself

Taking a look at the function generated from template. The Run method receives the request data in the req variable, returns either a 200 OK or 400 Bad Request Error message

<div align="center">
  <img src="images/az204-functionlab-task1-httpexample-file.png" width="800"/>
</div>

### Task 3 — Run the function locally

In the terminal I started the function, 'func start', and once it's built and loaded, I goto 'http://localhost:7071/api/HttpExample' in my browser.

<div align="center">
  <img src="images/az204-functionlab-task3-local-run.png" width="800"/>
</div>

### Task 4 — Create Prerequisite Azure Resources

Creating the Function App in Azure

<div align="center">
  <img src="images/az204-functionlab-task4-create-app-plan1.png" width="800"/>
  <img src="images/az204-functionlab-task4-create-app-plan2.png" width="800"/>
  <img src="images/az204-functionlab-task4-create-app-plan3.png" width="800"/>
  <img src="images/az204-functionlab-task4-create-app-plan4.png" width="800"/>
</div>

### Task 5 — Deploy the Function project to Azure

<div align="center">
  <img src="images/az204-functionlab-task5-deploy-func.png" width="800"/>
  <img src="images/az204-functionlab-task6-invoke.png" width="800"/>
</div>

### Task 6 — Verifying the deployed Function on Azure

And we are live!

<div align="center">
   <img src="images/az204-functionlab-task6-browse.png" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ The fact I was able to do this 100% from the command line is incredible. Just a great feeling to have that kind of capability.

## Next Steps

☁️ Tomorrow, I move onto Developing for Azure Storage.

## Social Proof

[Linkedin Post]()
