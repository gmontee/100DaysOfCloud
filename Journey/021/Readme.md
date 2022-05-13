<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/3rgXBN6i9LIUg6lSLe/giphy.gif" width="300"/>
</div>

# Day 21 - Azure AZ-204 Construct a Polyglot Data Solution

## Introduction

☁️ Today, I'm going to create an app that will pull information from Cosmos DB, and images from a blob container, to populate my application.

## Prerequisite

☁️ Ployglot means knowing multiple languages. In the case of this lab, it means using two cloud services for our application; one from the Cosmos DB, and the other from blob storage.

## Use Case

<div id="use case" align="center">
  <img src="https://microsoftlearning.github.io/AZ-204-DevelopingSolutionsforMicrosoftAzure/Instructions/Labs/media/Lab04-Diagram.png" width="600"/>
</div>

- Develop solutions that use Cosmos DB storage
  - **select the appropriate API and SDK for a solution**
  - implement a partitioning scheme and partition keys
  - **perform operations on data and Cosmos DB containers**
  - set the appropriate consistency level for operations
  - manage change feed notifications

## Cloud Research

☁️ Since Cosmos DB is a Platform-as-a-Service item, upon creation it autogenerates endpoints, keys, and connection strings for easy interaction.

☁️ Similar to yesterday, instead of Storage, I added the Microsoft Azure Cosmos package so my .NET code could interact with that API.

## My Experience with Cosmos DB

### Task 0 — Create Prerequisite Resources

Creating the Cosmos DB

<div align="center">
  <img src="images/az204-coslab-task0-create-cosmos.png" width="800"/>
</div>

Getting the Cosmos DB URI, primary key, and primary connection string

<div align="center">
  <img src="images/az204-coslab-task0-db-keys.png" width="800"/>
</div>

Need a storage account

<div align="center">
  <img src="images/az204-coslab-task0-storage-account.png" width="800"/>
</div>

### Task 1 — Upload images to Azure Blob Storage

Creating a container for the images

<div align="center">
  <img src="images/az204-coslab-task1-create-container.png" width="800"/>
</div>

Uploading the images

<div align="center">
  <img src="images/az204-coslab-task1-upload-images.png" width="800"/>
</div>

### Task 2 — Create a Cosmos DB database and collection, and perform a JSON data upload

Taking a look at the construction of the JSON data I'm working with

<div align="center">
  <img src="images/az204-coslab-task2-json-data.png" width="800"/>
</div>

Adding the Azure Cosmos DB .NET client library to the AdventureWorks.Upload project

<div align="center">
  <img src="images/az204-coslab-task2-add-cosmos-library.png" width="800"/>
</div>

Some of the code for creating the Cosmos database and container

<div align="center">
  <img src="images/az204-coslab-task2-create-cosmos-db-code.png" width="800"/>
</div>

Creating...

<div align="center">
  <img src="images/az204-coslab-task2-create-cosmos-db.png" width="800"/>
</div>

### Task 3 — Validate JSON data upload

Going to Data Explorer within the Cosmos DB

<div align="center">
  <img src="images/az204-coslab-select-sql-query.png" width="800"/>
</div>

Executing a select query

<div align="center">
  <img src="images/az204-coslab-select-sql-query-results.png" width="800"/>
</div>

### Task 4 — Configure a .NET web application

Updating appsettings.json with primary connection string and blob url

<div align="center">
  <img src="images/az204-coslab-task4-appsettings.png" width="800"/>
</div>

Code to accessing the container and finding products

<div align="center">
  <img src="images/az204-coslab-task4-create-context.png" width="800"/>
</div>

### Task 5 — Configure connectivity to Azure Cosmos DB

Running the app locally

<div align="center">
  <img src="images/az204-coslab-task5-running-app-locally.png" width="800"/>
</div>

### Task 6 — Validate that the .NET application successfully connects to data stores

Here I can see my app is reaching out to the Cosmos DB in Azure, to pull the information and images about the various products. Note: not all products had images for them

<div align="center">
  <img src="images/az204-coslab-task6-data-loaded.png" width="800"/>
</div>

## ☁️ Cloud Outcome

Just incredible! I was able to populate a database with a schema json file, upload images to a container, and retrieve the info and images from the app.

## Next Steps

Tomorrow, I'm going to learn about implementing user authentication and authorization in Azure

## Social Proof

[Linkedin Post]()
