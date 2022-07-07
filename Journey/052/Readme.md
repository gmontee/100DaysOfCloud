<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/3rTUE3BHqcYxhtWYyb/giphy.gif" width="300"/>
</div>

# Day 52 - Ansible - Working with Roles

## Introduction

☁️ Today, I'm going to be working with roles in Ansible

## Prerequisite

☁️ Roles allow you to reuse content such as vars, files, tasks, handlers, and other Ansible artifacts

## Use Case

<div id="use case" align="center">
  <img src="https://adamtheautomator.com/wp-content/uploads/2021/09/image-110.png" width="600"/>
</div>

## Cloud Research

- Nagios is an open-source application to monitors systems, networks, and infrastructure

## My Experience

### Task 1 — Create a Role

Creating a role names "baseline"; I goofed the first time, forgetting the roles directory.

`mkdir /etc/ansible/roles/baseline/{template,tasks,files}`

<div align="center">
  <img src="images/ansible-roles-task1-create-role-1.png" width="800"/>
</div>

### Task 2 — Configure the Role to Deploy MOTD

Copying a previously made template to our new baseline's template directory

<div align="center">
  <img src="images/ansible-roles-task2-motd-2.png" width="800"/>
</div>

Writing the short task to utilize our motd template

<div align="center">
  <img src="images/ansible-roles-task2-motd-3.png" width="800"/>
</div>

Adding our deploy motd task to the main playbook

<div align="center">
  <img src="images/ansible-roles-task2-motd-4.png" width="800"/>
</div>

### Task 3 — Configure the Role to Install Nagios Client

Creating and editing a task for install the Nagios client

<div align="center">
  <img src="images/ansible-roles-task3-nagios-5.png" width="800"/>
</div>

Using Yum to install the latest version of the Nagios client

<div align="center">
  <img src="images/ansible-roles-task3-nagios-6.png" width="800"/>
</div>

Adding our install nagios task to the main playbook

<div align="center">
  <img src="images/ansible-roles-task3-nagios-7.png" width="800"/>
</div>

### Task 4 — Configure the Role to add Nagios entry

Creating and editing the edit hosts playbook

<div align="center">
  <img src="images/ansible-roles-task4-nagios-entry-9.png" width="800"/>
</div>

Creating a task to add the Nagios server info to the hosts file

<div align="center">
  <img src="images/ansible-roles-task4-nagios-entry-10.png" width="800"/>
</div>

Adding our add server entry task to the main playbook

<div align="center">
  <img src="images/ansible-roles-task4-nagios-entry-11.png" width="800"/>
</div>

### Task 5 — Configure the Role to Create noc User

Creating and editing playbook to create noc user

<div align="center">
  <img src="images/ansible-roles-task5-noc-user-12.png" width="800"/>
</div>

Adding task to import the noc user's public key

<div align="center">
  <img src="images/ansible-roles-task5-noc-user-13.png" width="800"/>
</div>

Adding our create noc user task to the main playbook

<div align="center">
  <img src="images/ansible-roles-task5-noc-user-14.png" width="800"/>
</div>

### Task 6 — Deploy the Role

Just needed to add the roles reference to our web playbook

<div align="center">
  <img src="images/ansible-roles-task6-deploy-role-15.png" width="800"/>
</div>

Showtime!

<div align="center">
  <img src="images/ansible-roles-task6-deploy-role-16.png" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ Roles give the ability to create a template that is modular, loose-coupling, allowing you to edit the role as needed without changing the main playbook

## Next Steps

☁️ Tomorrow, I'm going to put it all together by deploying a web server, with confidential data stored in an Ansible vault

## Social Proof

[Linkedin Post]()
