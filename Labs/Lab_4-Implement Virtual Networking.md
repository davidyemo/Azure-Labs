Lab_4- Implement Virtual Networking


Task 1: Create a Virtual Network with Subnets using the Portal


Created a virtual network named CoreServicesVnet in the East US region with the address space 10.20.0.0/16, and configured two subnets — SharedServicesSubnet (10.20.10.0/24) and DatabaseSubnet (10.20.20.0/24). 
Exported and downloaded the deployment template (template.json) for future use.

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab4-Pic1.png?raw=true)


Task 2: Create a Virtual Network and Subnets using a Template


Modified the exported template.json and parameters.json files to define a new virtual network ManufacturingVnet (10.30.0.0/16) with SensorSubnet1 (10.30.20.0/24) and SensorSubnet2 (10.30.21.0/24). 
Deployed the customized ARM template in Azure to create the new network and verified successful deployment.

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab4-Pic2.png?raw=true)
![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab4-Pic3.png?raw=true)

Task 3: Create and configure communication between an Application Security Group and a Network Security Group.


Created an Application Security Group (asg-web) and a Network Security Group (myNSGSecure) associated with the SharedServicesSubnet in CoreServicesVnet. 
Configured an inbound NSG rule to allow TCP traffic (ports 80, 443) from the ASG and an outbound rule to deny internet access.

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab4-Pic4.png?raw=true)
![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab4-Pic5.png?raw=true)
![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab4-Pic6.png?raw=true)

Task 4: Configure Public and Private Azure DNS Zones


Created a public DNS zone (contozino.com) with an A record (www.contozino.com → 10.1.1.4) to verify external name resolution. 
Then created a private DNS zone (private.contozino.com), linked it to ManufacturingVnet, and added an A record (sensorvm → 10.1.1.4) for internal name resolution.

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab4-Pic7.png?raw=true)
![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab4-Pic8.png?raw=true)
![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab4-Pic9.png?raw=true)

Verified the host name www.contozino.com resolves to the IP address by checking in command prompt. The image bellow shows resolution is working correctly.

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab4-Pic10.png?raw=true)



