<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/SWWi6avzV08in1M2gR/giphy.gif" width="500"/>
</div>

# Day 44 - Ansible - Playbooks

## Introduction

Today, I'm going to learn about utilizing Playbooks in Ansible

## Prerequisite

☁️ Ansible Playbook - a blueprint of automation tasks, which are complex IT actions executed with limited or no human involvement

## Use Case

<div id="use case image" align="center">
  <img src="https://k21academy.com/wp-content/uploads/2020/07/Ansible-playbook.png" width="500"/>
</div>

- Playbook: one or more plays
  - Play: maps a group of hosts to tasks that used to call Ansible modules
    - Task(s): unit(s) of action

## Cloud Research

☁️ Use Cases: regularly used to automate IT infrastructure (such as operating systems and Kubernetes platforms), networks, security systems, and developer personas (such as Git)

☁️ Playbooks declare configurations and orchestrate steps to ensure the remote resources are configured as expected

☁️ Written tasks can be run synchronously or asynchronously

☁️ Utilizing Playbooks means it can be source controlled

## My Experience

### Task 1 — Creating a Playbook to install Apache

Setting up my inventory file

<div align="center">
  <img src="images/ansible-playbook-hosts-1.png" width="800"/>
</div>

Creating a playbook to install an Apache HTTP Server

<div align="center">
  <img src="images/ansible-playbook-apache-2.png" width="800"/>
</div>

Running the playbook we see a change on node1; the "Gathering Facts" task is built-in and Ansible uses it to collect information about the managed node(s)

`ansible-navigator run apache.yml -i hosts`

<div align="center">
  <img src="images/ansible-playbook-run-playbook-3.png" width="800"/>
</div>

SSHing into node1 I can manually check that httpd is installed (I could've also just used an Ad Hoc Ansible command)

`rpm -qi httpd`

<div align="center">
  <img src="images/ansible-playbook-httpd-4.png" width="800"/>
</div>

### Task 2 - Expanding the Playbook to enable httpd

I'm expanding the Apache playbook to not only install httpd, but enable it

<div align="center">
  <img src="images/ansible-playbook-apache-enabled-5.png" width="800"/>
</div>

YAML files are sensitive to spacing. In this case there was a space in front of the dash starting the name line.

<div align="center">
  <img src="images/ansible-playbook-apache-error-6.png" width="800"/>
</div>

Alright, now we're in business. SSHing back into node1 I can check the status of the Apache HTTP Server

`systemctl status httpd`

<div align="center">
  <img src="images/ansible-playbook-apache-success-7.png" width="800"/>
</div>

### Task 3 - Expanding the Playbook to copy web.html over

Adding a html file I can use to copy to webservers

<div align="center">
  <img src="images/ansible-playbook-webhtml-8.png" width="800"/>
</div>

I'm extending the playbook file again to now copy the web.html I just created

<div align="center">
  <img src="images/ansible-playbook-addcopy-9.png" width="800"/>
</div>

Success again! Utilizing curl I can see the html page on node1

`curl http://node1`

<div align="center">
  <img src="images/ansible-playbook-copysuccess-10.png" width="800"/>
</div>

I went to the Apache playbook and changes hosts from node1 to webserver; now when I run the playbook it now affects node2; this is a good example of a playbook being idempotent

<div align="center">
  <img src="images/ansible-playbook-allhosts-11.png" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ Good Playbooks are idempotent, meaning repeated execution always leads to the same result.

☁️ Once you have a playbook written, it's amazing to think all the work it's saving you by not having to manually log into each server, perform the tasks, etc, and hope you don't make any mistakes.

## Next Steps

Next, I'm going to learn about leveraging variables in Ansible

## Social Proof

[Linkedin Post](link)
