# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
 
 VM is infrastructure as a service (IaaS) and its more expensive. Multiple VMs can grouped together to provide high availability and scalability.

 App service is Platform as a Service (PaaS). It provides high availability and auto-scaling. The scalling can be vertical by allocate and de-acclocate resources such as RAM and CPU, or horizental by create or stope instance of app. App service have some constraints in case of scalability, it not provide pay as you go, the payemnt for service plan even if not used.

 costs: 
I used the pricing service "https://azure.microsoft.com/en-in/pricing/calculator/" for below comparison:

App service: Monthly: $244.55 
Premium V3 Tier; 1 P1V3 (2 Core(s), 8 GB RAM, 250 GB Storage) x 730 Hours; Windows OS; 0 SNI SSL Connections; 0 IP SSL Connections

VM: Monthly: $148.97
1 D2 v5 (2 vCPUs, 8 GB RAM) x 730 Hours (Pay as you go), Windows (License included), OS Only; 0 managed disks – S4, 100 transaction units; Inter Region transfer type, 5 GB outbound data transfer from West US to East Asia


 scalability:
 - Autoscaling: app service has Built-in service while VM has Virtual machine scale sets.

 - Load balancer: the app service has integrated load balancer while the VM has Azure Load Balancer.

 - Scale limit: in app service the scale limit to 30 instances, 100 with App Service environment while vm support 1000 nodes per scale set in paltform images and 600 nodes per scale set in custom images. 

 Availability:
 the app service and VM can provide availability by existing in multi regions.
 
- *Choose the appropriate solution (VM or App Service) for deploying the app*
   
App service 

- *Justify your choice*

Since the application very simple and have a rest APIs theat inqury about data and not have a big processing of data. and we don't need to have a controle over OS or have to speceify the programming language that not supported by app service. 

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.

* If the app service not support the desired programming language.
* if we need more control over OS.
* if we need to have high computing resources, e.g. processing big data.
