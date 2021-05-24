# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

--------------------
#### Analysis

**Costs**:
In terns of cost, an App service would be mmore flexible since more than one app can be made to share
the App Service plan. A Virtual machine has the advantage of being able to be deallocated when not in use
in order to cut costs

**Scalability**:
Both the Virtual machine and the App Service can be scalled horizontally and vertically. VMs can be scalled horizontally using a VMSS, while App Service's have native Auto scalling properties

**Availability**:
In terms of availability Virtual machines generally have more availability than App Services, but require extra setup and configuration to be fault tolerant and avoid downtimes during maintenance and upgrades

**Workflow**:
It is fairly easier to deploy applications to App Service than it is to Virtual Machines. Although an automated CI/CD pipeline could be designed to resolve this issue, overhead time would be spent in the process

--------------------
#### Decision

Deployment option: App Service ([https://article-cms-app.azurewebsites.net/](https://article-cms-app.azurewebsites.net/))

--------------------
#### Justification

An App Service is a PaaS offering meaning that you just have to deploy your code and not worry about the underlying infrastructure. The application is designed to be cloud native removing the need for server management and optimization. It also has good pricing tiers and gives adequate room for scalability. Another caveat is the wide range of deployment options available that can easily be integrated into a production workflow

--------------------

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.*

App Service's are limited 14 GB of Memory and 4 VCPUs. If the application were to be a high compute application the need to extend hardware requirements would call for a Virtual Machine. A need to utilize custom monitoring and logging solutions could also necessitate a shift to VMs. Also if the application has dependencies to specific softwares on a server then a VM would be more suitable.
