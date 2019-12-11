Datadog is the essential monitoring platform for cloud infrastructure, applications, and logs. We bring together data from servers, containers, databases, and third-party services to make your stack entirely observable. By adding this extension, you'll be able to utilize any monitors in Datadog to stop problematic deployments in their tracks by adding Datadog Monitors as [gates](https://docs.microsoft.com/en-us/azure/devops/pipelines/release/approvals/gates?view=azure-devops) in your Azure Pipelines.

Not using Datadog yet? [Learn more or get started today with a 14 day free trial!](https://www.datadoghq.com/)

# Example Scenario:

Consider a canary deployment that updates an e-commerce website in stages across different regions. To ensure the update was successful before rolling it out to the next region, you might want to check the status of various health indicators in the recently updated region, such as:

- the memory and CPU utilization of hosts in that region
- the number of error logs from your shopping cart application
- the results of an automated browser check, which verifies that the website’s regional endpoint loads quickly and responds correctly to simulated user actions  

In Datadog, you could create individual monitors for everything you want to know about, and then combine them using a [composite monitor](https://docs.datadoghq.com/monitors/monitor_types/composite/), using simple logic statements to specify a desired combination of monitor conditions. Then, you can set that composite monitor as a gate between the two stages of a pipeline to automatically stop a deployment if an unhealthy state is detected in Datadog.


![Datadog Gates](https://imgix.datadoghq.com/img/blog/monitor-azure-devops/monitor-azure-devops-gates-deployment-setup.png)


However you define the health of your service, using Datadog monitors as gates in Azure DevOps can help you ensure that your deployments go off without a hitch.

# Other Resources

In addition to this extension, we also have the [Datadog Service Hooks integration](https://marketplace.visualstudio.com/items?itemName=Datadog.datadog-integration) that enables you to monitor Azure DevOps builds, releases, code events, and work items in Datadog.

For more information about using Datadog and Azure DevOps together, check out our [blog](https://datadoghq.com/blog/monitor-azure-devops/) and [documentation](https://docs.datadoghq.com/integrations/azure_devops/).

To view the source code for this extension, visit our [repo](https://github.com/DataDog/azure-devops-monitor-gate-extension).