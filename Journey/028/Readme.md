<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/r2MkQEOe7niGk/giphy.gif" width="500"/>
</div>

# Day 28 - Azure AZ-204 Enhance a web application by using the Azure Content Delivery Network

## Introduction

☁️ Today, I'm going to update a web app to use Content Delivery Network to serve multimedia content and to serve the web application itself

## Prerequisite

☁️ Content Delivery Network (CDN) is a distributed network of servers that can efficiently deliver web content to users

## Use Case

<div id="use case" align="center">
  <img src="https://microsoftlearning.github.io/AZ-204-DevelopingSolutionsforMicrosoftAzure/Instructions/Labs/media/Lab12-Diagram.png" width="600"/>
</div>

- Implement caching for solutions
  - configure cache and expiration policies for Azure Cache for Redis
  - **implement secure and optimized application cache patterns including data sizing, connections, encryption, and expiration**

## Cloud Research

☁️ Designed to send audio, video, apps, photos, and other files using servers closet to each user

- Benefits of using a CDN
  - better performance
  - improved user experience for end users
  - large scaling to better handle instantaneous high loads
  - distribution of users requests
  - serving content directly from edge servers, instead of origin server

## My Experience

### Step 0 — Create Prerequisite Resources

Create a Storage account

<div align="center">
  <img src="images/az204-cdnlab-task0-create-storage.png" width="800"/>
</div>

Create a web app by using Azure App Service

<div align="center">
  <img src="images/az204-cdnlab-task0-create-web-app.png" width="800"/>
  <img src="images/az204-cdnlab-task0-create-web-app1.png" width="800"/>
</div>

### Task 1 — Configure Content Delivery Network and endpoints

Register the Microsoft.CDN provider

<div align="center">
  <img src="images/az204-cdnlab-task1-register-cdn.png" width="800"/>
</div>

Create a Content Delivery Network profile

<div align="center">
  <img src="images/az204-cdnlab-task1-create-cdn-profile.png" width="800"/>
  <img src="images/az204-cdnlab-task1-create-cdn-profile1.png" width="800"/>
</div>

Configure Storage containers

<div align="center">
  <img src="images/az204-cdnlab-task1-container.png" width="800"/>
</div>

Create Content Delivery Network endpoints

<div align="center">
  <img src="images/az204-cdnlab-task1-endpoint.png" width="800"/>
  <img src="images/az204-cdnlab-task1-endpoint1.png" width="800"/>
</div>

### Task 2 — Upload and configure static web content

Observe the landing page

<div align="center">
  <img src="images/az204-cdnlab-task2-observe-landing.png" width="800"/>
</div>

Upload Storage blobs

<div align="center">
  <img src="images/az204-cdnlab-task2-upload-files.png" width="800"/>
</div>

Configure Web App settings

<div align="center">
  <img src="images/az204-cdnlab-task2-configure-app" width="800"/>
</div>

Validate the corrected landing page

<div align="center">
  <img src="images/az204-cdnlab-task2-validate-landing.png" width="800"/>
</div>

### Task 3 — Use Content Delivery Network endpoints

Retrieve endpoint Uniform Resource Identifiers (URIs)

<div align="center">
  <img src="images/az204-cdnlab-task3-retrieve-uri.png" width="800"/>
</div>

Test multimedia content

<div align="center">
  <img src="images/az204-cdnlab-task3-test-link.png" width="800"/>
</div>

Update the Web App settings

<div align="center">
  <img src="images/az204-cdnlab-task3-update-endpoint.png" width="800"/>
</div>

Test the web content

<div align="center">
  <img src="images/az204-cdnlab-task3-test-cdn-link.png" width="800"/>
  <img src="images/az204-cdnlab-task3-test-cdn-link1.png" width="800"/>
</div>

## Next Steps

Tomorrow, I'm going to take the AZ-204 Azure Developer exam!

## Social Proof

[Linkedin Post](https://www.linkedin.com/posts/georgemontee_github-gmontee100daysofcloud-activity-6935590185220915200-rM9G?utm_source=linkedin_share&utm_medium=member_desktop_web)
