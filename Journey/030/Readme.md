<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/26zz9Wgu0FZxF5hzW/giphy.gif" width="500"/>
</div>

# Day 30 - Introduction to Docker

## Introduction

Today, I'm going to start learning about Docker

## Prerequisite

☁️ Docker is an open-source utilize that automates the deployment and management of programs inside software containers

## Use Case

<div id="use case image" align="center">
  <img src="https://jfrog--c.documentforce.com/servlet/servlet.ImageServer?id=01569000008kq46&oid=00D20000000M3v0&lastMod=1631618766000" width="500"/>
</div>

## Cloud Research

☁️ Docker Engine is an application used to build, run, and manage Docker containers

☁️ Docker Daemon is a component that listens to and processes API requests

☁️ Docker Client is the primary user interface

☁️ Docker Images are lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries, and settings

☁️ Docker Container is a virtualized runtime environment where users can isolate applications from the underlying system

☁️ Docker Registry is a storage and distribution system for Docker images

## My Experience

### Task 1 — Install Docker Engine via it's repository

First, I need to make sure everything is up-to-date, and then ensure prerequisites are installed

- ca-certificates: used to verify identity of 3rd parties, and encrypt data between you and them
- curl: stands for client URL; used to download/upload data using protocols like HTTP, HTTPS, SCP, SFTP, and FTP
- gnupg: stands for GNU Privacy Guard; used to encrypt files or sign files for integrity and authenticity
- lsb-release: lsb stands for Linux Standard Base; common runtime environment for 3rd party packages

<div align="center">
  <img src="images/docker-start-update-1.png" width="1000"/>
</div>

Now, I need to add Docker's official GPG key, which in the next step will be used to authenticate the repository

<div align="center">
  <img src="images/docker-start-prereqs-2.png" width="1000"/>
</div>

Adding the docker repository

<div align="center">
  <img src="images/docker-start-add-repo-3.png" width="1000"/>
</div>

Now to install the Docker Engine

- Docker-CE: community edition of the docker engine
- Docker-CE-CLI: command line interface for docker engine
- Containerd.io: daemon, manages the complete container lifecycle of it's host system
- Docker.Compose-plugin: tool for defining and running multi-container Docker applications

<div align="center">
  <img src="images/docker-start-install-engine-4.png" width="1000"/>
  <img src="images/docker-start-install-engine-5.png" width="1000"/>
</div>

I initially had trouble running the Hello World image, so I had to start the docker service

<div align="center">
  <img src="images/docker-start-hello-world-6.png" width="1000"/>
</div>

## ☁️ Cloud Outcome

☁️ To answer the question "What problem does Docker solve?", it simplifies the process of installing, running, and distributing software.

- A containerized application is more portable and can be deployed nearly anywhere.
- Containers do not contain an operating system, thus have a smaller footprint, making it faster to create and start
- Containers support isolation requirements, since they are independent
- Higher scalability since many containers can be placed on a single host

## Next Steps

Next I'm going to jump into it and run some containers!

## Social Proof

[Linkedin Post](https://www.linkedin.com/posts/georgemontee_github-gmontee100daysofcloud-activity-6937399986305327104-xoYq?utm_source=linkedin_share&utm_medium=member_desktop_web)
