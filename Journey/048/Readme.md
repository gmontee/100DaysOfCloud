<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/I7Il0qBnjThAI/giphy-downsized-large.gif" width="300"/>
</div>

# Day 48 - Ansible - Working with Confidential Data

## Introduction

Today, I'm going to learn about working with confidential data in Ansible

## Prerequisite

<div id="cover photo" align="center">
  <img src="https://miro.medium.com/max/1400/1*P5CDychkYdcq1qj5wl0ujg.jpeg" width="500"/>
</div>

☁️ Ansible Vault encrypts variables and files to protect sensitive data like usernames, passwords, and other secrets

## Cloud Research

☁️ Encryption for Ansible Vault only protects 'data at rest'; responsiblity for 'data in use' falls under play and plugin authors

☁️ Ansible recommends utilizing the attribute 'no_log', either for a task or the entire playbook, to prevent sensitive data spilling out during verbose logging mode

☁️ Ansible also recommends securing your text editors, like vim, emacs, by disabling the system clipboard, creation of backup files, autosaving, etc

## My Experience

### Task 1 — Encrypt a secret

Encrypting the secret file

`ansible-vault encrypt /home/ansible/secret`

<div align="center">
  <img src="images/ansible-vault-task1-encrypt-secret-1.png" width="800"/>
</div>

Trying to view the file, just shows an encrypted hash

<div align="center">
  <img src="images/ansible-vault-task1-encrypt-secret-2.png" width="800"/>
</div>

### Task 2 — Execute a Playbook using a Vault Password File

Being prompted for a password when runing playbooks hinders automation; since my server is secure, I create a vault file containing the password, which the playbook will reference

<div align="center">
  <img src="images/ansible-vault-task2-create-password-file-3.png" width="800"/>
</div>

Executing the playbook...

<div align="center">
  <img src="images/ansible-vault-task2-execute-playbook-4.png" width="800"/>
</div>

### Task 3 — Verify secure page deployed correctly

Attempting to curl the page without password shows an authorized page; entering the correct password shows the actual page

`curl -u bond http://node1/secure/classified.html`

<div align="center">
  <img src="images/ansible-vault-task3-verify-secure-5.png" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ Doing some more research, Ansible recommends not using the decrypt command, unless you want to do so permanently. For viewing or editing such files or playbooks, there's ansible-vault view, and ansible-vault edit

☁️ If you don't want to include the file path during command runtime, there's an environment variable that can be set

☁️ If you do use a vault password file, ensure it's added to .gitignore to avoid being committed to source control

## Next Steps

Next, I'm going to learn about renewing IAM access keys in Ansible

## Social Proof

[Linkedin Post](https://www.linkedin.com/posts/georgemontee_100daysofcloud-activity-6948314019367718912-BhwV?utm_source=linkedin_share&utm_medium=member_desktop_web)
