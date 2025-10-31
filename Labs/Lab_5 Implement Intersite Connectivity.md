## Implement Intersite Connectivity

This lab focused on establishing and managing connectivity between Azure virtual networks to enable secure communication across sites.

## Task 1: Create a core services virtual machine and a virtual network.

Created CoreServicesVM in East US with CoreServicesVnet (10.0.0.0/16) and Core subnet (10.0.0.0/24).

![logo](https://github.com/davidyemo/Azure-Labs/blob/main/Labs/All-Files/lab5-pic1.png?raw=true)


## Task 2: Create a virtual machine in a different virtual network.

Deployed ManufacturingVM in ManufacturingVnet (172.16.0.0/16) with Manufacturing subnet (172.16.0.0/24).

## Task 3: Use Network Watcher to test the connection between virtual machines

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/lab5-pic2.png?raw=true)
![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/lab5-pic3.png?raw=true)

Used Connection Troubleshoot to test connectivity between both VMs result in connectivity test showed unreachable as the VNETS were in separate networks.


## Task 4: Configure virtual network peerings between virtual networks

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/lab5-pic4.png?raw=true)


![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/lab5-pic5.png?raw=true)

Created peering between CoreServicesVnet and ManufacturingVnet; verified Connected status and confirmed communication via Network Watcher.

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/lab5-pic6.png?raw=true)

## Task 5: Use Azure PowerShell to test the connection between virtual machines

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/lab5-pic7.png?raw=true)

Ran Test-NetConnection <CoreServicesVM IP> -Port 3389 from ManufacturingVM — test succeeded after peering setup.

## Task 6: Create a custom route

Added perimeter subnet (10.0.1.0/24) and created route table rt-CoreServices with route to 10.0.0.0/16 via Network virtual appliance (10.0.1.7).
Associated route table with Core subnet.

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/lab5-pic8.png?raw=true)


![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/lab5-pic9.png?raw=true)

## Outcome
✅ Result: Intersite connectivity between VNets was fully established and verified, demonstrating effective cross-network communication and routing control in Azure.
