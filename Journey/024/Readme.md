<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/KpOqvmCFdNMhF0pQb7/giphy.gif" width="300"/>
</div>

# Day 24 - Azure AZ-204 Create a multi-tier solution by using Azure services

## Introduction

☁️ Today, I'm going to use the app services to deploy an app from an image, using httpbin which is a open source HTTP request and response service. I'll create an API proxy to manupiate requests and responses using the Azure API Management service.

## Prerequisite

☁️ Azure API Management helps organizations publish APIs to external, partner, and internal developers to unlock the potential of their data and services

## Use Case

<div id="use case" align="center">
  <img src="https://microsoftlearning.github.io/AZ-204-DevelopingSolutionsforMicrosoftAzure/Instructions/Labs/media/Lab08-Diagram.png" width="600"/>
</div>

- Implement API Management
  - create an APIM instance
  - create and document APIs
  - configure authentication for APIs
  - define policies for APIs

## Cloud Research

- Azure API Management is made of the following components:
  - API Gateway
    - Accepts API calls and routes them to your backend(s)
    - Verifies API keys, JWT tokens, certificates, and other credentials
    - Enforces usage quotas and rate limits
    - Transforms your API on the fly without code modifications
    - Caches backend responses where set up
    - Logs call metadata for analytics purposes
  - Azure Portal
    - Define or import API schema
    - Package APIs into products
    - Set up policies like quotas or transformations on the APIs
    - Get insights from analytics
    - Manage users
  - Developer Portal
    - Read API documentation
    - Try out an API via the interactive console
    - Create an account and subscribe to get API keys
    - Access analytics on their own usage

☁️ Products - Open (No subscription needed)r Protected (Subscription required)

☁️ Groups: Administrators, Developers, Guests (prospective customers)

☁️ Policies - allow the Azure Portal to change the behavior of the API through configuration

- Gateway design patterns

  - Gateway routing: reverse proxy, layer 7 routing
  - Gateway aggregation: calls multiple backend services, aggregates results to send back to client
  - Gateway Offloading: offload functionality from individual services
    - SSL termination
    - Authentication
    - IP allow/block list
    - Client rate limiting
    - Logging and Monitoring
    - Response Caching
    - GZIP compression
    - Servicing static content

- Policy Configuration

  - Inbound: applied to request
  - Backend: applied before the request is forwarded
  - Outbound: applied to response
  - On-error

- Subscription Key: a unique auto-generated key that can be passed through in the headers of the client request or as a query string parameter
  - can be scoped for all APIs, a single API, or a Product
  - 401 Access Denied response if key isn't passed

## My Experience

### Task 1 — Create Azure App Service resource using Docker container image

Create a web app by using Azure App Service resource by using an httpbin container image

<div align="center">
  <img src="images/az204-apilab-task1-create-app.png" width="800"/>
  <img src="images/az204-apilab-task1-create-app1.png" width="800"/>
</div>

Test the httpbin web application

<div align="center">
  <img src="images/az204-apilab-task1-http-test1.png" width="800"/>
  <img src="images/az204-apilab-task1-http-test2.png" width="800"/>
  <img src="images/az204-apilab-task1-http-test3.png" width="800"/>
  <img src="images/az204-apilab-task1-http-test4.png" width="800"/>
</div>

### Task 2 — Build an API proxy tier by using Azure API Management

Create an API Management resource

<div align="center">
  <img src="images/az204-apilab-task2-apim.png" width="800"/>
</div>

Define a new API

<div align="center">
  <img src="images/az204-apilab-task2-define-api.png" width="800"/>
  <img src="images/az204-apilab-task2-define-api1.png" width="800"/>
  <img src="images/az204-apilab-task2-define-api2.png" width="800"/>
  <img src="images/az204-apilab-task2-define-api3.png" width="800"/>
  <img src="images/az204-apilab-task2-define-api4.png" width="800"/>
  <img src="images/az204-apilab-task2-define-api5.png" width="800"/>
</div>

Manipulate an API response

<div align="center">
  <img src="images/az204-apilab-task2-api-manipulate.png" width="800"/>
  <img src="images/az204-apilab-task2-api-manipulate1.png" width="800"/>
  <img src="images/az204-apilab-task2-api-manipulate2.png" width="800"/>
  <img src="images/az204-apilab-task2-api-manipulate3.png" width="800"/>
  <img src="images/az204-apilab-task2-api-manipulate4.png" width="800"/>
</div>

## ☁️ Cloud Outcome

- For API Management pricing tiers, all of them have a 99.95% or better SLA, with the exception of the developer tier, which has no SLA.
  - Consumption is priced based per 10K calls
  - Other tiers are charged by the hour, provide scale-out units, caches and maximum throughput in increasing size

## Next Steps

Tomorrow, I'm going to learn about Event Grid

## Social Proof

[Linkedin Post]()
