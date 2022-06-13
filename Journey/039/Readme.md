<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/KdrSWXS2JovQjS17fq/giphy.gif" width="500"/>
</div>

# Day 39 - Docker Networking

## Introduction

Today, I'm going to learn about networking in Docker

## Prerequisite

☁️ Docker provides a number of ways to connect containers and services, and even non-Docker workloads, together

## Use Case

<div id="use case image" align="center">
  <img src="https://miro.medium.com/max/1400/1*WKiEgPXO8XXppoqgr7ZVQA.png" width="400"/>
</div>

## Cloud Research

☁️ Container Networking Model (CNM) - specification proposed by Docker where there is a network controller that is responsible for pairing a driver to a network; each driver is responsible for managing the network it owns

- CMN Concepts
  - Sandbox: an isolated unit containing all networking components associated with a single container
  - Endpoint: connects a sandbox to a network; each sandbox/container can have any number of endpoints, but has exactly one endpoint for each network it's connect to
  - Network: a collection of endpoints connected to one another
  - Network Driver: handles the actual implementation of the CNM concepts
  - IP Address Management (IPAM) Driver: automatically allocates subnets and IP addresses for networks and endpoints

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

☁️ I

## Next Steps

Next, I'm going to learn about security in Docker

## Social Proof

[Linkedin Post](link)
