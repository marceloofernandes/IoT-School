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

![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2516.42.44.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2516.43.56.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2516.44.07.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2516.44.32.png)


## Module 2: Customize the UX

Duration: 8 minutes

Instructions: https://docs.microsoft.com/en-us/azure/iot-accelerators/iot-accelerators-remote-monitoring-customize


##### Prepare a local development environment for the UI

The following steps outline the process to set up a local environment for UI development:       



1. Deploy a basic instance of the solution accelerator using the pcs CLI. Make a note of the name of your deployment and the credentials you provided for the virtual machine. For more information, see Deploy using the CLI.

![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2517.13.15.png)

2. To enable SSH access to the virtual machine that hosts the microservices in your solution, use the Azure portal or the Azure Cloud Shell. For example:

![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2517.17.06.png)


3. Use the Azure portal or the Azure Cloud Shell to find the name and public IP address of your virtual machine. For example:     

![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2517.19.48.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2517.21.01.png)

4. Use SSH to connect to your virtual machine. Use the IP address from the previous step, and the credentials you provided when you ran pcs to deploy the solution. The ssh command is available in the Azure Cloud Shell.       
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2517.27.53.png)

5. To allow the local UX to connect, run the following commands at the bash shell in the virtual machine:     
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2517.29.02.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2517.29.09.png)

6. After you see the command completes and the web site starts, you can disconnect from the virtual machine.

The web site did not start.


7. In your local copy of the azure-iot-pcs-remote-monitoring-webui repository, edit the .env file to add the URL of your deployed solution

![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2517.34.32.png)

...

9. To install the required libraries and run the UI locally, run the following commands:    


![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2517.39.08.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2517.39.59.png)


10. The previous command runs the UI locally at http://localhost:3000/dashboard. You can edit the code while the site is running and see it update dynamically.    

![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2517.40.50.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2415.29.48.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2415.29.58.png)

#### Customize the layout

![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2415.43.24.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2415.46.29.png)


<br />

#### Duplicate and customize an existing control

![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2415.53.45.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2415.55.28.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2416.02.00.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2416.07.13.png)

Failed to compile
./src/components/pages/dashboard/dashboard.js
Attempted import error: 'CustAlertsPanelContainer' is not exported from './panels' (imported as 'CustAlertsPanel').

![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2416.14.45.png)

![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2416.14.55.png)

#### Customize the telemetry chart


![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2416.19.01.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2416.20.58.png)


#### Add a new KPI

![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2416.24.27.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2416.26.06.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2416.28.49.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2416.29.55.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2416.30.48.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2416.34.24.png)
![alt text](https://github.com/marceloofernandes/IoT-School/blob/master/IoT-School-Customize-the-Remote-Monitoring-solution-to-accelerate-your-development/Remote%20Monitoring/Picture2416.37.30.png)


***(work in progress)***

## Module 3: Customize and redeploy a microservice

Duration:  4 minutes

Instructions: https://docs.microsoft.com/en-us/azure/iot-accelerators/iot-accelerators-microservices-example

<br />

#### Call the API and view response status




## Module 4: Integrate with visualization tools

Duration: 6 minutes

Instructions: Provided link is broken. Used this one instead: https://docs.microsoft.com/en-us/azure/iot-accelerators/iot-accelerators-remote-monitoring-integrate-time-series-insights

<br />



## Module 5: Connect your data to Azure Data Lake storage

Duration: 4 minutes

Instructions: https://docs.microsoft.com/en-us/azure/iot-accelerators/iot-accelerators-integrate-data-lake
