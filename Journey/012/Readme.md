<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/Wk5YYh2evQnNS/giphy.gif" width="500"/>
</div>

# Day 12 - Azure AZ-104 Implement Traffic Management

## Introduction

☁️ Yesterday's lab was focused on creating a unified mesh topology. Today, I will create a hub and spoke network topology, and use a load balancer and application gateway to route traffic via the hub.

## Prerequisite

☁️ When I was creating the mesh topology, I had to create network peerings to the other networks, and repeat the process on each VNet. With the Hub-and-Spoke topology, the "hub" will manage the connections.

## Use Case

<div id="use case" align="center">
  <img src="https://microsoftlearning.github.io/AZ-104-MicrosoftAzureAdministrator/Instructions/media/lab06.png" width="600"/>
</div>

- This architecture diagram is taken from the lab page, showing the three tasks:
  - Task 1: Provision the lab environment
  - Task 2: Configure the hub and spoke network topology
  - Task 3: Test transitivity of virtual network peering
  - Task 4: Configure routing in the hub and spoke topology
  - Task 5: Implement Azure Load Balancer
  - Task 6: Implement Azure Application Gateway

## Cloud Research

- ☁️ [Hub-Spoke topology](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/hybrid-networking/hub-spoke?tabs=cli) is where there's a hub virtual network acting as a central point of connectivity, usually where core services are deployed. The spoke virtual networks peer with the hub, and are used to isolate workloads.

- ☁️ [Azure Load Balancer](https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview) are used to distribute incoming network traffic across a group of resources. This service operates at Layer 4 of the OSI model.

- ☁️ [Azure Application Gateway](https://docs.microsoft.com/en-us/azure/application-gateway/overview), similar to the concept of a Load Balancer. However, Application Gateways operate at OSI Layer 7, enabling URL-based routing.

## My Experience

### Task 1 — Provision the lab environment

<div align="center">
  <img src="images/" width="800"/>
</div>

### Task 2 — Configure the hub and spoke network topology

<div align="center">
  <img src="images/" width="800"/>
</div>

### Task 3 — Test transitivity of virtual network peering

<div align="center">
  <img src="images/" width="800"/>
</div>

### Task 4 — Configure routing in the hub and spoke topology

<div align="center">
  <img src="images/" width="800"/>
</div>

### Task 5 — Implement Azure Load Balancer

<div align="center">
  <img src="images/" width="800"/>
</div>

### Task 6 — Implement Azure Application Gateway

<div align="center">
  <img src="images/" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ Result) Describe your personal outcome, and lessons learned.

## Next Steps

☁️ Tomorrow, I'm going to work with Azure Storage

## Social Proof

[Linkedin Post]()
