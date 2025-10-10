Azure Web App Deployment

Task 1: Create and Configure Web App

An Azure Web App was created using PHP 8.2 on Linux in the East US region with a Premium V3 P1V3 plan under the resource group `az104-rg9`.  

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/lab9a-pic1.png?raw=true)

Task 2: Create and Configure Deployment Slot

A staging deployment slot was added without cloning settings, and it was confirmed that the URL differed from the production slot.  

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/lab9a-pic2.png?raw=true)

Task 3: Configure Web App Deployment Settings

The staging slot was configured for continuous deployment from the GitHub repository `https://github.com/Azure-Samples/php-docs-hello-world` on the master branch, displaying "Hello World" upon verification.  

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/lab9a-pic3.png?raw=true)

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/lab9a-pic4.png?raw=true)

Task 4: Swap Deployment Slots

The staging slot was swapped with the production slot, resulting in the production app displaying "Hello World," and the default domain URL was recorded for load testing

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/lab9a-pic5.png?raw=true)
![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/lab9a-pic6.png?raw=true)

