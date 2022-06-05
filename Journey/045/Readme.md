<div id="cover photo" align="center">
  <img src="" width="500"/>
</div>

# Day 45 - Ansible - Tasks

## Introduction

Today, I'm going to learn about

## Prerequisite

☁️ Ansible tasks are a way to run adhoc commands against our inventory in a one-line single executable. Tasks are the basic building block of Ansible's execution and configuration.

## Use Case

<div id="use case image" align="center">
  <img src="https://linuxhandbook.com/content/images/2020/10/ansible-ad-hoc-command.png" width="500"/>
</div>

`$ ansible [pattern] -m [module] -a "[module options]"`

## Cloud Research

☁️ [Ansible Modules](https://docs.ansible.com/ansible/2.9/modules/modules_by_category.html) provide reusable, standalone scripts. For instance, under the Cloud module, there are scripts for running commands on AWS, Azure, Google Cloud, Docker, VMWare, etc. Another example is the Files module, enabling such capability as fetching, copying, finding, replacing, etc files.

## My Experience

### Task 1 — Summary of Step

Here I attempt to ping all the resources in my inventory, and for the non-local resources I get a permission denied

<div align="center">
  <img src="images/ansible-tasks-ping-all-1.png" width="800"/>
</div>

In the Ansible config file, I set the default remote user, which since I'm using AWS is ec2-user. I also tell Ansible where to find the needed ssh key. Finally, I disable host key checking, since I don't want an interactive experience when using Ansible

<div align="center">
  <img src="images/ansible-tasks-ping-all-2.png" width="800"/>
</div>

I received a warning, where Ansible found a Python interpreter at a certain path, but warns that might change with installation of another future Python interpreter. For now, I add a line to silence the warning.

<div align="center">
  <img src="images/ansible-tasks-ping-all-3.png" width="800"/>
</div>

### Task 2 — Summary of Step

Here I'm trying different commands, with two potential return codes, e.g., 0 (success), 1 (failure)

<div align="center">
  <img src="images/ansible-tasks-exit-codes-4.png" width="800"/>
</div>

Getting the UID of each of the created users

<div align="center">
  <img src="images/ansible-tasks-get-uid-5.png" width="800"/>
</div>

I'm changing the Message of the Day for the web servers, and then looking at the message

<div align="center">
  <img src="images/ansible-tasks-motd-6.png" width="800"/>
  <img src="images/ansible-tasks-motd-7.png" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️

## Next Steps

Next, I'm going to learn about

## Social Proof

[Linkedin Post](link)
