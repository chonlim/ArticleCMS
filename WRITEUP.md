# Resource Justification

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*

- *Analyze costs, scalability, availability, and workflow*

|Virtual Machine (VM)| Criteria  | Web App Service
|--|--|--|
| Higher than App Service. The maintaining, updating, configuring of VM is more labor intensive and time consuming. | Costs | Lower than VM. The costs vary depending on selected Plan (Dev/Test, Production, Isolated), which has to always be paid regardless if the application is running. |
| Various flexible options on CPU, RAM and Storage, depending on demand. For instance, selection range from 1 virtual CPU to several hundreds of virtual CPU. | Scalability | Offer auto-scaling, where vertical and horizontal scaling is possible. |
| High availability by grouping multiple virtual machines together. | Availability | Limited hardware availability, e.g. support up to maximum 4 vCPUs and 14 GB of RAM. |
| Infrastructure as a service (IaaS). Deployment can be done with custom images and host them directly on virtual machine. Existing on-premises application and environment can be easily migrated to virtual machine. | Workflow | Platform as a Service (PaaS). Provide continuous deployment model, where developer can link the Web App Service with GitHub (or other repo) during development and test phases. |



- *Choose the appropriate solution (VM or App Service) for deploying the app*

I select **Web App Service** to deploy the Article CMS application.


- *Justify your choice*

The Article CMS application is currently **light weight** and does **not require high performance computation**, which can be easily supported by the hardware limitation of Azure Web App Service. Also, the Article CMS application is unlikely to have high security requirements and **does not need a dedicated server**. Due to the **lower costs**, I would think Azure Web App Service to be the best choice to deploy the application.


### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

I would consider to migrate the Article CMS application from Web App Service to Virtual Machine, if:

 - Rapid increase in number of users and posts, which requires higher performance in computation power
 - New functions added to the application, which are only available in languages that are not supported by Azure Web App Service (e.g. C/C++)
 - New functions added, that requires special software installation and integration. For example, GPS services to locate the articles and plot them on a world map.

---

answered by: Chong Kiat Lim (chong_kiat.lim@mercedes-benz.com)