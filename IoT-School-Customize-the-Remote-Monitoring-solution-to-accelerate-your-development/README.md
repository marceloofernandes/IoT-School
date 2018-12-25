# IoT School: Customize the Remote Monitoring solution to accelerate your development

## Description:
This hands-on lab is part of the **IoT School** learning path about Azure IoT solutions provided by **Microsoft**. Its goal is to `"This path focuses on how to customize the Remote Monitoring solution. The series begins with showing you how to deploy the Remote Monitoring solution accelerator to your local machine for testing and development. Once your development environment is set up, you are shown how to customize the UX by accessing the source code, and how to customize and redeploy one of the microservices in the Remote Monitoring solution. And finally, you will learn about out-of-box data visualization capabilities in the Remote Monitoring solution as well as how to connect your data to an Azure Data Lake storage." ` It is available at https://iotschool.microsoft.com/learning-paths/6fNCiqwLIsemUAGuGUseYG .        

<br />
This task was performed by following each module instruction. Key screenshots are presented to demonstrated the obtained results along with some comments whenever applicable.    

<br />



## 5 Modules:

Total duration: 26min  

<br />



## Module 1: Run your environment locally

Duration: 4 minutes

Instructions: https://docs.microsoft.com/en-us/azure/iot-accelerators/iot-accelerators-remote-monitoring-deploy-local      

<br />



## Module 2: Customize the UX

Duration: 8 minutes

Instructions: https://docs.microsoft.com/en-us/azure/iot-accelerators/iot-accelerators-remote-monitoring-customize


##### Prepare a local development environment for the UI

The following steps outline the process to set up a local environment for UI development:       



1. Deploy a basic instance of the solution accelerator using the pcs CLI. Make a note of the name of your deployment and the credentials you provided for the virtual machine. For more information, see Deploy using the CLI.

(insert screenshots)

2. To enable SSH access to the virtual machine that hosts the microservices in your solution, use the Azure portal or the Azure Cloud Shell. For example:


(insert screenshots)

3. Use the Azure portal or the Azure Cloud Shell to find the name and public IP address of your virtual machine. For example:     



4. Use SSH to connect to your virtual machine. Use the IP address from the previous step, and the credentials you provided when you ran pcs to deploy the solution. The ssh command is available in the Azure Cloud Shell.       


5. To allow the local UX to connect, run the following commands at the bash shell in the virtual machine:     


6. After you see the command completes and the web site starts, you can disconnect from the virtual machine.

The web site did not start.


7. In your local copy of the azure-iot-pcs-remote-monitoring-webui repository, edit the .env file to add the URL of your deployed solution

...

10. The previous command runs the UI locally at http://localhost:3000/dashboard. You can edit the code while the site is running and see it update dynamically.    



#### Customize the layout



<br />

#### Duplicate and customize an existing control



Failed to compile
./src/components/pages/dashboard/dashboard.js
Attempted import error: 'CustAlertsPanelContainer' is not exported from './panels' (imported as 'CustAlertsPanel').

#### Customize the telemetry chart



#### Add a new KPI



***(work in progress)***

## Module 3: 

Duration:  minutes

Instructions: 

<br />



## Module 4: 

Duration:  minutes

Instructions: 

<br />



## Module 5: 

Duration:  minutes

Instructions: 
