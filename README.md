# HERE Maps & Location Services Data Streams on Azure Workshop

In this workshop you will deploy a simple web application that enables users to track the fleet of Contoso Corp. and allows to monitor various engine parameters on HTML using graphical representation. The application allows users to generate various engine parameters and location parameters which are used for fleet tracking and fleet health management. 

The application architecture uses [Azure ARM templates](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-quickstart-create-templates-use-the-portal), [Azure Event Hub](https://docs.microsoft.com/en-us/azure/event-hubs/), [Azure Serverless Functions](https://azure.microsoft.com/en-in/services/functions/), [Azure PowerShell](https://docs.microsoft.com/en-us/powershell/azure/overview?view=azps-1.8.0), [Azure Cosmos DB](https://azure.microsoft.com/en-in/services/cosmos-db/) and [Azure Web App](https://azure.microsoft.com/en-in/services/app-service/web). A webapp based on node.js will be deployed to view the results on web browser. A node.js based producer script allows users to generate the dummy data. It also calls HERE geocoder serverless function to fetch the address of corresponding to a latitude and longitude combination which is stored in Cosmos DB. 

See the diagram below for a depiction of the complete architecture. 

  ![Architecture Diagram](Images/architecture.png)

### Modules

This workshop is divided into four modules. Each module describes a scenario of
what we're going to build and step-by-step directions to help you implement the
architecture and verify your work.

| Module        | Description |
|---------------|-------------|
| [1. ARM Template Deployment][ARM Template Deploy] | The HERE Location Services Data Streams Template is a Solution Template on Azure  |
| [2. Data Setup Producer][Data_Setup_Producer] | Uploading the Producer setup data to azure PowerShell  |
| [3. Data Setup WebApp][Data_Setup_WebApp] | Creating Azure web-app and uploading the setup data  |
| [4. Validation][Validation] | Launch the web-app URL via browser to see the dashboard on a real-time map  |




:warning: These modules are intended to be executed linearly.

After you have completed the workshop you can delete all of the resources that were created by following the [cleanup guide][cleanup].




[ARM Template Deploy]:1_ARM_Template_Deploy/
[Data_Setup_Producer]:2_Data_Setup_Producer/
[Data_Setup_WebApp]:3_Data_Setup_WebApp/
[Validation]:4_Validation/
[cleanup]: 5_CleanUp/
