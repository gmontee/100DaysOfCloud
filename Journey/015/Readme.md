<div id="cover photo" align="center">
  <img src="https://media.giphy.com/media/xdkXW7Scx6gus/giphy.gif" width="500"/>
</div>

# Day 15 - Azure AZ-204 Scale apps in Azure App Service

## Introduction

☁️ Yesterday's I looked at the various settings within the Azure App Service. Today, I'm going to learn how autoscale operates in the App Service

## Prerequisite

☁️ An important cloud function is the ability of resources to scale to accommodate varying workload sizes. Ideally, out when the need is great, and in when the demand lessens.

## Use Case

<div id="use case" align="center">
  <img src="https://aspblogs.blob.core.windows.net/media/scottgu/WindowsLiveWriter/AnnouncingthenewAzureAppService_122D1/image_4.png" width="600"/>
</div>

## Cloud Research

☁️ Autoscaling - a cloud process that adjusts available resources based on the current demand, scaling in and out.

☁️ The Azure App Service monitors the resource metrics of a web app it runs. It responds to changes by adding or removing additional web servers.

☁️ It doesn't change CPU size, memory, storage, etc, which is scaling up and down. Thus it might not be the best option for resource intensive processing.

☁️ Improves availability and fault tolerance. However, if there are few instances to begin with, there's less capacity to handle a surge as it takes time for additional instances to spin up.

<div align="center">
  <p>Enable Autoscaling</p>
  <img src="https://docs.microsoft.com/en-us/learn/wwl-azure/scale-apps-app-service/media/enable-autoscale.png" width="600"/>
</div>

☁️ An instance limit can be set to prevent runaway autoscaling.

☁️ Two options to trigger autoscale actions; multiple conditions can be created

- based on metrics
- based on schedule

☁️ If metric based, the following can be used

- CPU percentage
- Memory percentage
- Disk Queue Length
- Http Queue Length
- Data In
- Data Out

☁️ Autoscale actions have cool periods, specified in minutes.

<div align="center">
 <p>Creating Autoscale Rules</p>
  <img src="https://docs.microsoft.com/en-us/learn/wwl-azure/scale-apps-app-service/media/autoscale-rules.png" width="600"/>
</div>

☁️ Best Practices

1. Ensure the maximum and minimum values are different and have an adequate margin between them
2. Choose the appropriate statistic for your diagnostics metric
3. Choose the thresholds carefully for all metric types
4. Considerations for scaling when multiple rules are configured in a profile
5. Always select a safe default instance count
6. Configure autoscale notifications

## Next Steps

☁️ Tomorrow, I'm going to look at Azure App Service deployment slots

## Social Proof

[Linkedin Post]()
