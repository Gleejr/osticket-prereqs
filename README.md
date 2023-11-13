<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>
1. In the Azure portal, enter "resource groups" into the search bar above, then select the "Resource Groups" option.
</p>

<p>
  
  ![2023-11-07_20-25-09](https://github.com/Gleejr/Configure-ad/assets/148407820/7cc33271-8449-4308-807e-c30cb75d85a6) 
</p>


<p>
2. Select "Create" to initiate the creation of a new resource group.
</p>
  <p>
  
  ![image](https://github.com/Gleejr/Configure-ad/assets/148407820/12f10b7d-3861-4515-932b-ef475d904c35)
</p>


<p>
3. Enter OsTicket-Lab for the resource group and choose "West US 3" as the region. Click on "Review + Create" and then proceed to click on "Create" once more.
</p>
 
<p>
  <img width="781" alt="Screen Shot 2023-11-12 at 10 09 12 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/00cc4f18-92f7-44fa-9f9e-184dc9d1a4bf">
</p>


<p>
4. After creating the resource group, please enter "virtual machines" into the search bar above and proceed to select "Virtual Machines."
</p>

<p>
 <img width="888" alt="Screen Shot 2023-11-07 at 8 46 03 PM" src="https://github.com/Gleejr/Configure-ad/assets/148407820/504f8572-b736-4ef7-8b51-4b23baf6b49e">
</p>


<p>
5. Click on "create a virtual machine hosted by Azure". 
</p>

<p>
  <img width="622" alt="Screen Shot 2023-11-07 at 8 50 42 PM" src="https://github.com/Gleejr/Configure-ad/assets/148407820/650e51a1-27dd-436d-adb8-37db85bbc6bb">
</p>


<p>
6. Choose "OsTicket-Lab" as the resource group created in step 2. Enter "VM1" as the virtual machine name, select West US 3 as the region, and select the "Windows 10 pro" image. 
</p>

<p>
  <img width="772" alt="Screen Shot 2023-11-12 at 10 15 38 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/27099087-ce65-4b7c-b63a-f6ca18fbdaae">
</p>


<p>
7. Choose the "Standard_D4s_v3 - 4 vCPUs 16 GiB memory" size. Set "labuser" as the username and "Password1234" as the password.
</p>

<p>
  <img width="772" alt="Screen Shot 2023-11-12 at 10 18 30 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/1ff037b8-2971-48fb-930e-847e3e9821b4">
</p>


<p>
8. Click on "Review + Create," then proceed to click "Create" for the first virtual machine (DC-1).
</p>

<p>
  <img width="282" alt="Screen Shot 2023-11-07 at 9 20 18 PM" src="https://github.com/Gleejr/Configure-ad/assets/148407820/edbeace0-962d-4353-b7d2-ebc042b7cb01">
  <img width="363" alt="Screen Shot 2023-11-07 at 9 22 01 PM" src="https://github.com/Gleejr/Configure-ad/assets/148407820/d98e55e4-cca2-43c8-91a9-1024c243600f">
</p>

<p>
8. Go to virtual machines, go into VM1, and grab the public IP address.
</p>

<p>
  <img width="1291" alt="Screen Shot 2023-11-12 at 10 27 32 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/b7b24d9d-b47e-4de4-a4bb-36f4075d4cec">
</p>


<p>
9. Launch remote desktop and login into VM1 using the username and password that was set in step 7.
</p>

<p>
  <img width="711" alt="Screen Shot 2023-11-12 at 10 30 21 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/cb4fd3f5-d8d7-4518-a0f9-0aae864455d2">
  <img width="662" alt="Screen Shot 2023-11-12 at 10 30 47 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/22a3b02f-c2e0-4b47-8f22-8c0f194677f5">
</p>


<p>
10. Right click on the windows icon, select run, and type in control. 
</p>

<p>
  <img width="436" alt="Screen Shot 2023-11-12 at 10 41 03 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/23a04e74-7154-408b-b60c-3e87149a9136">
</p>

<p>
11. Click on programs and click on "Turn Windows features on and off"
</p>

<p>
  <img width="651" alt="Screen Shot 2023-11-12 at 10 45 57 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/8a577b33-f24a-4e95-87dd-e55f9bc96898">
  <img width="527" alt="Screen Shot 2023-11-12 at 10 45 04 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/23de8513-ce01-472b-9f66-bfc05fb086f3">
</p>


<p>
12. Click on Internet Information Services and expand it, expand World Wide Web Services, expand application development features, and check the boxnext to CGI.
</p>

<p>
  <img width="418" alt="Screen Shot 2023-11-12 at 10 49 28 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/c1d42803-707e-4e53-89ab-4d7efa4bd2ee">
  <img width="427" alt="Screen Shot 2023-11-12 at 10 50 34 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/5db8ae3b-f1fb-44ad-8b24-66a9f0a1fc13">
  <img width="416" alt="Screen Shot 2023-11-12 at 10 51 26 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/6ea5ed8d-6708-453d-80eb-eb518db2b7fd">
  <img width="406" alt="Screen Shot 2023-11-12 at 10 52 13 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/bd05881d-a6e7-45f4-b51d-e56d0668fd57">
</p>














