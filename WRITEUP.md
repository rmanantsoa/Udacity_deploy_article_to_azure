# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

--------------------
#### Analysis

##### **Costs**:
Azure VMs are more expensive to run in comparison to Azure App Service.
But we can turn VM in Deallocated state to save money on my Azure costs when we don’t need those VMs running.


##### **Scalability**:
Both the VM and the App Service can be scalled horizontally and vertically.
Azure App Service have constraints in comparison to Azure VMs in terms of scalability. Hence, Azure VMs are preferred for apps, which have scope to expand for future


##### **Availability**:
VM generally is more available than App services but we need do configure the VM to be fault tolerant and prevent downtimes during maintenances.

##### **Workflow**:


For workflow, it is really easier to deploy and use CI/CD pipeline on App service than VM.
Although we can configure an personalized automated CI/CD workflow on VM but require more configuration and more time to set up.

--------------------
#### My choice

I choose to use App service https://manantsoa-cms.azurewebsites.net

--------------------
#### Justification
It is really easy to create a link between github repo and App service deployement center, less time needed to configure a production workflow.
It is faster to configure App service than Virtual Machine. 
It is less expensive than VM and scalable. 

#### Assess app changes that would change your decision.
App service ressource limitation, with a big project who needed more ressources, I would choose VM.
