
Task 1: Create a Virtual Network with Subnets using the Portal
Created a virtual network named CoreServicesVnet in the East US region with the address space 10.20.0.0/16, and configured two subnets — SharedServicesSubnet (10.20.10.0/24) and DatabaseSubnet (10.20.20.0/24). 
Exported and downloaded the deployment template (template.json) for future use.

![logo]()


Task 2: Create a Virtual Network and Subnets using a Template
Modified the exported template.json and parameters.json files to define a new virtual network ManufacturingVnet (10.30.0.0/16) with SensorSubnet1 (10.30.20.0/24) and SensorSubnet2 (10.30.21.0/24). 
Deployed the customized ARM template in Azure to create the new network and verified successful deployment.

![logo]()
![logo]()

Task 3: Create and configure communication between an Application Security Group and a Network Security Group.
Created an Application Security Group (asg-web) and a Network Security Group (myNSGSecure) associated with the SharedServicesSubnet in CoreServicesVnet. 
Configured an inbound NSG rule to allow TCP traffic (ports 80, 443) from the ASG and an outbound rule to deny internet access.

![logo]()
![logo]()
![logo]()

Task 4: Configure Public and Private Azure DNS Zones
Created a public DNS zone (contoso.com) with an A record (www.contoso.com → 10.1.1.4) to verify external name resolution. 
Then created a private DNS zone (private.contoso.com), linked it to ManufacturingVnet, and added an A record (sensorvm → 10.1.1.4) for internal name resolution.

![logo]()
![logo]()
![logo]()
![logo]()



