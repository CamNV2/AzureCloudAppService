# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*
--------------------
#### Analytics

**Costs**:
-Virtual Machine are only charged on disk costs when stopped.
-Azure App Service will continue charging even though apps are unused or when stopped.

**Scalability**:
-Both the Virtual machine and the App Service can be scalled horizontally and vertically.
+ In VMs, horizontal scaling is achieved via Scale Sets. If existing VM does not belong to Scale Set, might need a bit of configuration work to enable.
+ Azure App Service provides an integrated load balancer and can easily increase instances

**Availability**:
In terms of availability Virtual machines generally have more availability than App Services, but require extra setup and configuration to be fault tolerant and avoid downtimes during maintenance and upgrades

**Workflow**:
It is fairly easier to deploy applications to App Service than it is to Virtual Machines.

--------------------
#### My choice
I choose App Service because the CMS app is developed using python and App Service is very well supported and suitable for easy deploy through Azure.
Using App service I can quickly deploy my web application without creating programming environment and Virtual machines behaves like a full, separate computer that I am responsible for everything: maitenance, security, update etc.

--------------------

My Python App Service [https://articlecmsproject.azurewebsites.net/]
