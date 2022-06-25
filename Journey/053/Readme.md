<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/xFlfIdvz1fXHjmTQyC/giphy.gif" width="500"/>
</div>

# Day 53 - Ansible - Putting it Together

## Introduction

☁️ Today, I'm going to put it all together by deploying a web server, with confidential data stored in an Ansible vault

## Prerequisite

☁️ [Ansible Templates](../047/Readme.md)

☁️ [Ansible Confidential Data](../050/Readme.md)

## Use Case

<div id="use case" align="center">
  <img src="images/advanced-features-in-ansible-playbooks.png" width="800"/>
</div>

## Cloud Research

- LET'S GOOOOOOOOOOOOO!!

## My Experience

### Task 1 — Protect Confidential Information

Encrypting our confidential info

<div align="center">
  <img src="images/ansible-all-task1-secure-1.png" width="800"/>
</div>

### Task 2 — Playbook to deploy httpd

Creating and editing the deploy httpd playbook

<div align="center">
  <img src="images/ansible-all-task2-deploy-httpd-2.png" width="800"/>
</div>

The webserver playbook; handler restarts the httpd daemon that is flagged by both installation and service manipulation for httpd

<div align="center">
  <img src="images/ansible-all-task2-deploy-httpd-3.png" width="800"/>
</div>

### Task 3 — Deploy templates to webservers group

Task for deploying the vhost.conf.j2 and htpasswd.j2 templates

<div align="center">
  <img src="images/ansible-all-task3-deploy-templates-4.png" width="800"/>
</div>

### Task 4 — Asynchronously execute data-job on webservers

Task for executing data-job script with a timeout of 600 seconds and no polling

<div align="center">
  <img src="images/ansible-all-task4-async-tasks-5.png" width="800"/>
</div>

### Task 5 — Execute the Playbook

Success

<div align="center">
  <img src="images/ansible-all-task5-execute-6.png" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ Although, this is the 13th day of Ansible, there's still a lot for me to learn and master

## Next Steps

☁️ Tomorrow, I'm going to reflect on my journey so far

## Social Proof

[Linkedin Post]()
