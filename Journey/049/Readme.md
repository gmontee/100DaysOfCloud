<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/N8Th40N8MW1iM/giphy.gif" width="300"/>
</div>

# Day 49 - Ansible - Renewing IAM Access Keys

## Introduction

Today, I'm going to learn about renewing IAM access keys in Ansible

## Prerequisite

☁️ Access keys are long-term credentials for an IAM user or the AWS account root user

## Use Case

<div id="cover photo" align="center">
  <img src="https://www.ansible.com/hs-fs/hubfs/Screen%20Shot%202022-05-05%20at%209.55.59%20AM.png?width=670&name=Screen%20Shot%202022-05-05%20at%209.55.59%20AM.png" width="500"/>
</div>

## Cloud Research

☁️ Access keys consist of two parts, the access key ID, and the secret access key

☁️ AWS's recommended best practice is to use temporary security credentials, e.g., IAM roles, instead of access keys. However, if you do use them, they recommend rotating them every 90 days

## My Experience

### Task 1 — Create the Playbook

I log into AWS, and there's my current Access Key ID, ending in UWV4

<div align="center">
  <img src="images/ansible-iam-task1-view-current-1.png" width="800"/>
</div>

Now, to create the playbook. First task is to get the current access key

<div align="center">
  <img src="images/ansible-iam-task1-create-keyupdate-2.png" width="800"/>
  <img src="images/ansible-iam-task1-create-keyupdate-3.png" width="800"/>
</div>

Next task, remove that original key

<div align="center">
  <img src="images/ansible-iam-task1-create-keyupdate-4.png" width="800"/>
</div>

Create our new key

<div align="center">
  <img src="images/ansible-iam-task1-create-keyupdate-5.png" width="800"/>
</div>

We need to store the new key's access key id and the secret itself

<div align="center">
  <img src="images/ansible-iam-task1-create-keyupdate-6.png" width="800"/>
</div>

### Task 2 — Execute the Playbook

Executing the playbook...

<div align="center">
  <img src="images/ansible-iam-execute-playbook-7.png" width="800"/>
</div>

### Step 3 — Verify Key Change

Refreshing the AWS IAM page, I see a new key, ending in 6VV5

<div align="center">
  <img src="images/ansible-iam-new-key-8.png" width="800"/>
</div>

## ☁️ Cloud Outcome

☁️ E

## Next Steps

Next, I'm going to reflect on my journey so far.

## Social Proof

[Linkedin Post](link)
