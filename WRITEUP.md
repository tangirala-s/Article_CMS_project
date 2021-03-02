# https://ozarticlecms.azurewebsites.net

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*

**Analyze costs, scalability, availability, and workflow**

- *Cost Analysis* : The cost of running a VM and App Service were compared using the Microsoft Azure price estimator tool. Price for a month of running the services (720 hours), in the same geo-location "Australia Southeast", and the basic available compute options on both of them with the same underlying OS (Linux-Ubuntu) I find that the virtual machine is costing me about 4 times as much as an app Service.

![Price Comparision](https://github.com/tangirala-s/Article_CMS_project/blob/master/Screenshot-Images/price-compare.png)

- *Scalability* : VM scaling needs the use of scale sets, maintenance and reconfiguration whenever we scale the application. App Service lets us use auto-scaling both horizontal and vertical based on usage.

- *Availability* : To achieve high availability while using VMs multiple VMs must be grouped together and maintained. Whereas an App Service has high availability as its default feature.

- *Workflow* : With the VM we have more control of the underlying Operating System environment and more infrastructure control can be enforced, but this makes it difficult to push updates to the application whenever changes are made. An app service can utilize the continuous-deployment using github to easily push changes.

**Choose the appropriate solution (VM or App Service) for deploying the app**
I choose to deploy this application using an Azure **App Service**

**Justify your choice**
*In this Scenario the best choice is to use an App Service to deploy the application, considering the flexibility in maintenance and low costs involved. More importantly we do not need the environment control that VM offers in this scenario*

### Assess app changes that would change your decision.
If in the future, this application builds into one with more functionalities and the security of application becomes more of a concern I might consider redeploying it using a VM. If the development stage of the application is completed and I have a stable version that I can host without expecting many changes after deployment, I might consider a VM.
