# Implementation Validation 

In this module, you are going to access the Azure Web App to view the dashboard which we have created in the previous module. You will be able to access two seperate Dashboards, one to track the Fleet movement and another one to view the engine health parameters. 

### Implementation

In our previous modules we have created Web App. We assume that you have completed all the previous modules successfully. In this module you are going to execute the producer script to generate the data and then you will view the fleet movement of the vehicles on the dashboard by running the azure web app.

## 1. Steps to Execute Producer

<details>
<summary><strong>Step-by-step instructions (expand for details)</strong></summary><p>
 
1. Open Azure Portal home page.

1. Click on **Cloud shell** to open the Azure PowerShell command-line.

  	![HERE Maps & Location Services Data Streams](../Images/1_AzureHome_CloudShell.png)

1. It may take few seconds for **PowerShell command-line** to be configured for your account.

	![HERE Maps & Location Services Data Streams](../Images/2_PowershellCommandline.png)
	
1. By default, the path of PowerShell will be in the Azure directory. We need to set location to our home directory to execute our Producer script. Execute the below command to set location to your home path.

                >Set-Location $home 
	
		
6. Above command would have changed the current path and it should be set as your home path.


1. Navigate to the **Producer** directory by executing the below command.

                >cd Producer
	
  
1. You can simulate up to 10 Trucks to generate the data. You can mention the number of trucks by mentioning it as an argument in the command line. You can mention any value between 1-10.

              	>node producer.js 8

	![HERE Maps & Location Services Data Streams](../Images/10_ProducerResultConsole_2.png)
  
  
 1. Keep this window open so that producer can keep generating the data.
  
</p></details>

## 2. Steps to Execute Web App

<details>
<summary><strong>Step-by-step instructions (expand for details)</strong></summary><p>

1. Open the browser tab and enter the Web App URL which you copied/saved in the previous module. It will be similar to below format. 

 		Eg: https://fleetdashboard.azurewebsites.net

1. You should be able to see the Map dashboard. Based on your truck count in the producer script, the Truck icons will be displayed on the Map.

1. You should be able to see simulated movement of the vehicles on the dashboard.

  	![HERE Maps & Location Services Data Streams](../Images/3_DashboardOutput.PNG)

1. To access the Line Graph dashboard, type /graph in the URL and access the same in the web browser. 

              Eg: https://fleetdashboard.azurewebsites.net/graph
              
    ![HERE Maps & Location Services Data Streams](../Images/4_DashboardOutput_Graph.PNG)


1. It will open a web page where you can select any vehicle from the dropdown. 

    ![HERE Maps & Location Services Data Streams](../Images/5_DashboardOutput_Graph_Select.PNG)
    
1. Click on textbox to select the vehicle. 

    ![HERE Maps & Location Services Data Streams](../Images/6_DashboardOutput_Graph_Select.png)
    
1. Select the Truck and click on Submit button, it will plot the Line graph of Engine Temperature, Engine RPM, Engine Load and Coolant Temperature.

    ![HERE Maps & Location Services Data Streams](../Images/7_LineGraph_DashboardOutput.PNG)
    
    
    ![HERE Maps & Location Services Data Streams](../Images/8_LineGraph_DashboardOutput.PNG)

  
</p></details>




Congratulations You have completed the Workshop successfully..!
  
After you have completed the workshop you can delete all of the resources that were created by following the [cleanup guide][cleanup].



[cleanup]: ../5_CleanUp/


