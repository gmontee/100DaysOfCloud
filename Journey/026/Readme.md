<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/L8Pt775dNHcgo/giphy.gif" width="500"/>
</div>

# Day 26 - Azure AZ-204 Asynchronously process messages by using Azure Service Bus Queues

## Introduction

☁️ Today, I'm going to read and delete messages from the Azure Service Bus queue using the .NET library

## Prerequisite

☁️ Azure Service Bus is a fully managed enterprise message broker with message queues and publish-subscribe topics

## Use Case

<div id="use case" align="center">
  <img src="https://microsoftlearning.github.io/AZ-204-DevelopingSolutionsforMicrosoftAzure/Instructions/Labs/media/Lab10-Diagram.png" width="600"/>
</div>

- Develop message-based solutions
  - **implement solutions that use Azure Service Bus**
  - implement solutions that use Azure Queue Storage queues

## Cloud Research

☁️ Service Bus: provides messaging services between applications, services, and devices

☁️ Messages are received and processed in a First-in, First-out fashion

☁️ Azure Event Hub versus Azure Service Bus: initially they sound similar, but Azure Event Hub is geared for ingesting big data via events, where as Azure Service Bus focuses on messages; Something has happened versus do or give me something

## My Experience

### Step 0 — Create Prerequisite Resources

I need to create an Azure Service Bus namespace, and a Service Bus Queue

<div align="center">
  <img src="images/az204-buslab-task0-create-bus.png" width="800"/>
</div>

Grabbing the primary connection string for later use

<div align="center">
  <img src="images/az204-buslab-task0-create-bus1.png" width="800"/>
  <img src="images/az204-buslab-task0-create-bus2.png" width="800"/>
</div>

Creating a message queue

<div align="center">
  <img src="images/az204-buslab-task0-create-bus3.png" width="800"/>
  <img src="images/az204-buslab-task0-create-bus4.png" width="800"/>
</div>

### Task 1 — Create a .NET Core project to publish messages to a Service Bus queue

Now, I'm creating a .NET app to publish messages into an Azure Service Bus queue

<div align="center">
  <img src="images/az204-buslab-task1-create-pub-app.png" width="800"/>
  <img src="images/az204-buslab-task1-create-pub-app1.png" width="800"/>
  <img src="images/az204-buslab-task1-create-pub-app2.png" width="800"/>
  <img src="images/az204-buslab-task1-create-pub-app3.png" width="800"/>
</div>

Publish messages to an Azure Service Bus queue

<div align="center">
  <img src="images/az204-buslab-task1-pub-messages.png" width="800"/>
  <img src="images/az204-buslab-task1-pub-messages1.png" width="800"/>
  <img src="images/az204-buslab-task1-pub-messages2.png" width="800"/>
  <img src="images/az204-buslab-task1-pub-messages3.png" width="800"/>
  <img src="images/az204-buslab-task1-pub-messages4.png" width="800"/>
</div>

### Task 2 — Create a .NET Core project to read messages from a Service Bus queue

Create a .NET project

<div align="center">
  <img src="images/az204-buslab-task1-read-messages.png" width="800"/>
  <img src="images/az204-buslab-task1-read-messages1.png" width="800"/>
  <img src="images/az204-buslab-task1-read-messages2.png" width="800"/>
  <img src="images/az204-buslab-task1-read-messages3.png" width="800"/>
</div>

Read messages from an Azure Service Bus queue

<div align="center">
  <img src="images/az204-buslab-task1-read-messages4.png" width="800"/>
  <img src="images/az204-buslab-task1-read-messages5.png" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ I went over to [Microsoft Docs for Azure.Message.ServiceBus namespace](Azure.Messaging.ServiceBus) to review the classes, constructors, properties, etc that were available.

## Next Steps

Tomorrow, I'm going to learn about streaming application metrics to Application Insights, and use that Service's dashboard to review performance details

## Social Proof

[Linkedin Post]()
