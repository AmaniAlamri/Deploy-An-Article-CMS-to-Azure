# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
 
 VM is infrastructure as a service (IaaS) and its more expensive. Multiple VMs can grouped together to provide high availability and scalability.

 App service is Platform as a Service (PaaS). It provides high availability and auto-scaling. The scalling can be vertical by allocate and de-acclocate resources such as RAM and CPU, or horizental by create or stope instance of app. App service have some constraints in case of scalability, it not provide pay as you go, the payemnt for service plan even if not used.

- *Choose the appropriate solution (VM or App Service) for deploying the app*
   
App service 

- *Justify your choice*

Since the application very simple and have a rest APIs theat inqury about data and not have a big processing of data. and we don't need to have a controle over OS or have to speceify the programming langige that not supported by app service. 

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.

* If the app service not support the desired programming language.
* if we need more control over OS.
* if we need to have high computing resources, e.g. processing big data.
