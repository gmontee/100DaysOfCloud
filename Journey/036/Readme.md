<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/xT0xepVmwUCPc9vKyQ/giphy.gif" width="500"/>
</div>

# Day 36 - Docker Registry

## Introduction

Today, I'm going to learn about Docker Registry

## Prerequisite

☁️ Docker Registry - a stateless, highly scalable server side application that stores and lets you distribute Docker images

## Use Case

<div id="use case image" align="center">
  <img src="https://4.bp.blogspot.com/-yeD6y92nmvc/W1SvdGaBHUI/AAAAAAAABcs/5EXkFqwbeVUh2guqQDvjJ-xbjf4BFaP1wCLcBGAs/s1600/private%2Bdocker%2Bregistry.jpg" width="600"/>
</div>

- Use Cases:
  - tightly control where your images are being stored
  - fully own your images distribution pipeline
  - integrate image storage and distribution tightly into your in-hose development window

## Cloud Research

☁️ Default public registry is [Docker Hub]{https://hub.docker.com/)

☁️ Options are Docker's open source registry software, or the Enterprise Solution, Docker Trusted Registry

☁️ htpasswd is used to create and update the flat-files used to store usernames and password for basic authentication of HTTP users

☁️ x.509 Certificate is a standard format for public key certificates that securely associate cryptographic key pairs with identities such as websites, individuals, or organizations

☁️ bcrypt is a password-hashing function based on the Blowfish cipher

## My Experience

### Task 1 — Set up Private Registry

Set up basic authentication; options used are -B (bcrypt encryption for passwords), -b (batch mode), -n (display the results on standard output)

<div align="center">
  <img src="images/docker-registry-task1-createhtpasswd-1.png" width="800"/>
</div>

Creating self-signed certificates

<div align="center">
  <img src="images/docker-registry-task1-createcerts-2.png" width="800"/>
</div>

Creating the registry; mounting volumes for the certificate and password files

<div align="center">
  <img src="images/docker-registry-task1-createregistry-3.png" width="800"/>
</div>

### Task 2 — Test the registry from a docker workstation server

Need to trust the self-signed certificate, then test authentication against private registry

<div align="center">
  <img src="images/docker-registry-task2-trust-cert-4.png" width="800"/>
</div>

Pushing an image to the private registry

<div align="center">
  <img src="images/docker-registry-task2-push-image-5.png" width="800"/>
</div>

Pulling an image from the private registry

<div align="center">
  <img src="images/docker-registry-task2-pull-image-6.png" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ Setting up the Registry with all the environment variables seemed a bit tedious to me. Having worked in the Government sector, I can see the need for creating a private registry for images you want tight control for security reasons.

## Next Steps

Next, I'm going to learn about Docker Compose!

## Social Proof

[Linkedin Post](link)
