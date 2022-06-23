<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/jkZc8OAlapk8DFRNlA/giphy.gif" width="300"/>
</div>

# Day 47 - Ansible - Using Templates in Ansible

## Introduction

Today, I'm going to learn about utilizing Templates in Ansible

## Prerequisite

☁️ [Templates](https://docs.ansible.com/ansible/latest/user_guide/playbooks_templating.html) give the ability to define text files with variables instead of static values, and replace those variables at playbook runtime

## Use Case

<div id="cover photo" align="center">
  <img src="https://www.middlewareinventory.com/wp-content/uploads/2020/05/Screenshot-2020-05-18-at-9.50.17-AM.png" width="600"/>
</div>

## Cloud Research

☁️ Ansible templates are built on the [Jinja2 templating language](https://jinja.palletsprojects.com/en/3.1.x/) with a j2 file extension

## My Experience

### Task 1 — Insert Variable into Template

I have a template file for httpd.conf

<div align="center">
  <img src="images/ansible-template-task1-httpd-1.png" width="800"/>
</div>

I manually change all the /var/www/ references to {{ web dir }}, so the location reference can change as needed

<div align="center">
  <img src="images/ansible-template-task1-httpd-2.png" width="800"/>
</div>

### Task 2 — Create the Playbook

I create my playbook, and give a value to the variable 'webdir'

<div align="center">
  <img src="images/ansible-template-task1-template-yml-3.png" width="800"/>
  <img src="images/ansible-template-task1-template-yml-4.png" width="800"/>
</div>

Before I execute the playbook, I jump onto the web server and confirm there is no reference to 'opt'

<div align="center">
  <img src="images/ansible-template-task1-verify-current-5.png" width="800"/>
</div>

### Task 3 — Verify Results

Executing the playbook....

<div align="center">
  <img src="images/ansible-template-task1-execute-6.png" width="800"/>
</div>

Jumping back onto the web server, I can see that the file was updated to reference the 'opt' location

<div align="center">
  <img src="images/ansible-template-task1-verify-current-7.png" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ The copy function is usually used for copying files over, but utilizing templates, dynamically text files can be created on remote hosts

## Next Steps

Next, I'm going to learn about working with confidential data in Ansible

## Social Proof

[Linkedin Post](link)
