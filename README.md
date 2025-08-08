# Microsoft Sentinel and Microsoft Defender LAB
In this lab, I will be walking you through how to make use of Microsoft Defender for cloud and Microsoft Sentinel solution to harden your Azure Virtual machine security and also manage incidents

<h2>OVERVIEW</h2>

<p>Microsoft Sentinel is a scalable, cloud-native security information and event management (SIEM) that delivers an intelligent and comprehensive solution for SIEM and security orchestration, automation, and response (SOAR). Microsoft Sentinel provides cyberthreat detection, investigation, response, and proactive hunting, with a bird's-eye view across your enterprise.

<p>Microsoft Sentinel also natively incorporates proven Azure services, like Log Analytics and Logic Apps, and enriches your investigation and detection with AI. It uses both Microsoft's threat intelligence stream and also enables you to bring your own threat intelligence.

<p>Microsoft Defender for Cloud is a cloud-native application protection platform (CNAPP) that is made up of security measures and practices that are designed to protect cloud-based applications from various cyber threats and vulnerabilities. </p>


<h2>Platform Used</h2>

- <b>Azure Portal: https://portal.azure.com/</b> 
- <b>Microsoft Defender Portal: https://security.microsoft.com/</b>

<h2>Project-lab walk-through:</h2>

<p align="center">
1. Go to Azure portal: https://portal.azure.com/ 
<br>  
Note: I have two (2) Log Analytics workspaces at the moment. However, I’m going to create new one for this demo and name it Demo-workspace. See below screenshot for guide:
 
<br>

 ![image](https://github.com/user-attachments/assets/0db41cd3-7d57-4f44-9067-591fe7432a82) 
 <br>
 ![image](https://github.com/user-attachments/assets/21363dbe-dd63-4ed9-ac92-cada0f8a65ed)
<br/>
<br>
2. From Azure portal global search space, search for Defender for cloud: 
<br />
<br />
![image](https://github.com/user-attachments/assets/691cf1bd-2c89-4c07-8a09-8a3a44168efb)
<br />
<br />
3. Click on “Environment settings” and select the Demo-workspace created earlier
<br />
<br />
![image](https://github.com/user-attachments/assets/934b6897-4574-4700-9d86-a87984e49caf)
<br />
<br />
4. By default, the plans are turned ‘OFF’. Hence click on ‘ON’ and ‘save’
<br />
<br />
![image](https://github.com/user-attachments/assets/a796c8f7-b558-4c69-bb46-4c5f6e7af787)
<br />
<br />
5. Afterwards, you refresh the ‘Environment setting’ blade to see your plan changes
<br />
<br />
![image](https://github.com/user-attachments/assets/3c31e035-a938-4d1d-89a2-9d6b8b808305)
<br />
<br />
5. Next, go to the Azure virtual that exist in the same subscription where we enabled “Microsoft Defender for Cloud”
<br> By now, we can see the status is “ON” <br />
![image](https://github.com/user-attachments/assets/5924e365-024d-4d47-a1bd-1e0458522fe1)
<br />
<br />
We can see Recommendations and the severity of the impact.
<br> In addition, you can also check for alert on the resource in Microsoft Defender <br />
<br />
<br />
![image](https://github.com/user-attachments/assets/dc496ea8-a312-4793-a0e4-605ea7cfaeba)
<br />
<br />
6. Next, we will proceed to download a malware file for the purpose of testing effectiveness of the “Microsoft Defender for cloud” on the virtual machines and aslo to help the Cloud device administrator efficiently manage the security of the devices.
<br />
<br />
![image](https://github.com/user-attachments/assets/23cb1e56-68fa-4b92-a529-adc62357c5a0)
<br />
<br />
7. Next, I goto Microsoft Sentinel to add the demo-workspace
<br />
<br />
![image](https://github.com/user-attachments/assets/874ac8f7-0703-49c8-9079-fe21a0e661a0)
<br />
<br />
8. Next, select the workspace in sentinel
<br> Go to ‘content hub’ <br />
![image](https://github.com/user-attachments/assets/c730286e-9806-4e7e-bfb2-ae8ce3640d9c)
<br />
<br />
9. Search for ‘Microsoft defender for cloud’ and install
<br> Afterwards, refresh and you should be able to see this:
<br />
<br />
<br />
![image](https://github.com/user-attachments/assets/889ed745-7a6b-40fe-883e-b38222dc86dd)
<br />
<br />
10. Next, go to ‘Data Connectors’ blade and click on the first one:
<br />
<br />
![image](https://github.com/user-attachments/assets/3f28519c-ae4e-42d4-ac97-5d84fc884546)
<br />
<br />
11. Select the open connection page. Afterwards, turn on the button:
<br />
<br />
![image](https://github.com/user-attachments/assets/a1596245-d032-4520-97f4-fca5443d0b87)
<br />
<br />
12. Follow thesame process to add the connector: ‘Microsoft Defender XDR’
<br />
<br />
![image](https://github.com/user-attachments/assets/81d4024f-8073-4aa1-be0b-a5ef19b09977)
<br />
<br />
<br>Note: The connector can be enabled only on subscriptions that have at least one Microsoft Defender plan enabled in Microsoft Defender for Cloud, and only by users with Contributor permissions on the subscription.
<br />
<br />
13. Next, go to Microsoft 365 Defender page (here:{https://security.microsoft.com}) as it provides a summary of the incident, including assosciated alerts and categories, the scope, evidence, and other important information about the incident.
<br />
<br />
![image](https://github.com/user-attachments/assets/28ad1fe5-8304-4d42-bb5a-596fe5c4e69b)
<br />
<br />
Checking the Microsoft Sentinel Incidents blade, we can see the incident details as well:
<br />
<br />
![image](https://github.com/user-attachments/assets/00f6618b-2d43-4874-8797-b5503268562e)
<br />
<br />
The incident can be assigned to a security engineer for investigation and remediation steps.
<br />
<br />
<h2>REFERENCES:</h2>
<li>https://learn.microsoft.com/en-us/azure/sentinel/overview?tabs=azure-portal
<li>https://learn.microsoft.com/en-us/azure/defender-for-cloud/defender-for-cloud-introduction</li>
Thank you for following through!!!
<br />
