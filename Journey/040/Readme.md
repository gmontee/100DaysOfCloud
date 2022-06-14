<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/e05GB2c86qgOk/giphy.gif" width="400"/>
</div>

# Day 40 - Docker Security

## Introduction

Today, I'm going to learn about security in Docker

## Prerequisite

☁️ [Docker Content Trust (DCT)](https://docs.docker.com/engine/security/trust/) is a secure way to verify the integrity of images before you pull or run them

## Use Case

<div id="use case image" align="center">
  <img src="https://docs.docker.com/engine/security/trust/images/tag_signing.png" width="600"/>
</div>

## Cloud Research

☁️ Using DCT, the image creator can sign each image with a certificate, which clients can use to verify the image before running it

## My Experience

### Task 1 — Tag an Image

I'm just going to pull the hello world image, and tag it

<div align="center">
  <img src="images/docker-security-task0-image-0.png" width="800"/>
</div>

### Task 2 — Generate Trust Key

I need to login into Docker Hub, and then create the Trust Key

<div align="center">
  <img src="images/docker-security-task1-generate-key-1.png" width="800"/>
</div>

### Task 3 — Add a Signer

Adding myself as a signer to the repo

<div align="center">
  <img src="images/docker-security-task2-create-tag-2.png" width="800"/>
</div>

### Task 4 — Test

Pulling the image with DCT turned on

<div align="center">
  <img src="images/docker-security-task3-pull-image.png" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ Outcome

- Keys
  - Trust Key: identifies me as a user
  - Root Key: root of trust for repo, can be used for multiple repos
  - Repository Key: used to sign image tags

## Next Steps

Next, I'm going to learn about ...

## Social Proof

[Linkedin Post](link)
