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

<p>
13. Expand "Common HTTP Features" and make sure that every box is checked. Click OK and installation should start.
</p>

<p>
  <img width="418" alt="Screen Shot 2023-11-13 at 8 51 29 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/dde4e3d3-66d4-4021-85ff-f0d49c1ca333">
  <img width="659" alt="Screen Shot 2023-11-13 at 8 51 59 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/4f5ba23d-516a-48bf-97cf-e0240105d84f">
</p>

<p>
14. Once the installation has completed, open a web browser and type in 127.0.0.1. This can test if the web server is working by populating the defualt IIS website.
</p>

<p>
  <img width="724" alt="Screen Shot 2023-11-13 at 8 58 51 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/dcd410a0-11d8-4a97-a64d-cf16b40b839a">
</p>

<h3>Install PHP Manager for IIS</h3>

<p>
15. Once PHP Manager for IIS is downloaded, click next, I agree, and next again. Once it has successfully installed click close.
</p>

<p>
<img width="505" alt="Screen Shot 2023-11-13 at 9 07 57 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/29e09e0e-85b9-444c-a3cd-7ba6a037e721">
</p>

<h3>Install Rewrite Module</h3>

<p>
16. Once Rewrite Module is downloaded, select "I agree" and click install. Once it has successfully installed click close. 
</p>

<p>
<img width="501" alt="Screen Shot 2023-11-13 at 9 18 59 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/106a29b9-70b2-4b0b-95bb-c880ea5a8952">
</p>

<h3>Create a directory for PHP on the local hard drive</h3>

<p>
17. Open file exlporer, type in "c:" to go to the local drive. Create a new folder named "PHP". 
</p>

<p>
<img width="1122" alt="Screen Shot 2023-11-13 at 9 27 59 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/49e62e44-da2f-46a5-a60f-e87e5727fc39">
</p>

<p>
18. Once the PHP zip folder has downloaded, right click and select extract all.  
</p>

<p>
<img width="1130" alt="Screen Shot 2023-11-13 at 9 39 05 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/9dac114c-2762-44be-8c94-6a6d47874046">
</p>

<p>
19. Select browse and choose the PHP folder that was created in step 17.  
</p>

<p>
<img width="1130" alt="Screen Shot 2023-11-13 at 9 39 05 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/9dac114c-2762-44be-8c94-6a6d47874046">
</p>

<h3>Install VC_redist.x86</h3>

<p>
20. Once VC_redist.x86 has donloaded, select "I agree" and click install. Once it has successfully installed click close. 
</p>

<p>
<img width="483" alt="Screen Shot 2023-11-13 at 9 54 12 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/9a9efe57-1eb4-43d9-bd19-6f75d77a22e9">  
</p>

<h3>Install MySQL 5.5.62</h3>

<p>
21. Once MySQL 5.5.62 has donloaded, Click next, select "I agree", and click next.
</p>

<p>
<img width="501" alt="Screen Shot 2023-11-13 at 10 01 16 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/9195f2e4-45be-4f50-8b76-711e431572e7">
</p>

<p>
22. Choose "typical" for the setup type, click install, and keep clicking next until finish populates.
</p>

<p>
<img width="503" alt="Screen Shot 2023-11-13 at 10 03 53 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/eb821400-fbd5-4ecb-90da-2d29fac2ec67">
</p>

23. Click next, select "standard configuration", and click next until you reach a screen to create a password.
</p>

<p>
<img width="508" alt="Screen Shot 2023-11-13 at 10 07 51 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/8f6f4c6f-456b-4251-9373-0ddf27b1cb0e">
</p>

24. Create a password and click next. Click execute to begin installation. Once it has successfully installed click finish. 
</p>

<p>
<img width="500" alt="Screen Shot 2023-11-13 at 10 13 43 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/55437f9f-3cf1-4ca3-a256-5c23f7107913">
<img width="506" alt="Screen Shot 2023-11-13 at 10 14 44 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/5b8b7c77-d86d-4565-b29d-5de18364d593">
</p>

<h3>IIS Configurations</h3>

<p>
25. Go to the start menu and type in IIS. Run IIS as an administrator.
</p>

<p>
<img width="1440" alt="Screen Shot 2023-11-13 at 10 21 47 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/0cb553d2-8267-4beb-86df-5b2e6695d160">
</p>

<p>
26. Once IIS opens, double click on PHP Manager, and click on "Register new PHP version".
</p>

<p>
<img width="1440" alt="Screen Shot 2023-11-13 at 10 21 47 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/0cb553d2-8267-4beb-86df-5b2e6695d160">
<img width="1254" alt="Screen Shot 2023-11-13 at 10 26 55 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/91b54f41-9471-49ee-959a-db9da86630b8">
</p>

<p>
27. Click on the three dots, find the PHP folder that was created in step 17, select the "PHP-cgi" file, and press OK.
</p>

<p>
<img width="514" alt="Screen Shot 2023-11-13 at 10 29 48 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/3f48422e-4075-4663-a3c4-9feb4b2e7d20">
<img width="710" alt="Screen Shot 2023-11-13 at 10 33 55 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/4aa603fb-3e02-44ee-8ec7-1e502b4d6ede">
</p>

<p>
28. Go back to the main screen, click on the name of the server (VM1 "VM1/labuser") and click "Restart".
</p>

<p>
<img width="1254" alt="Screen Shot 2023-11-13 at 10 38 27 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/841458ea-4962-4f2f-8718-c31ef1cb22a8">
</p>

<h3>Install OsTicket</h3>
<p>
29. Once OsTicket zip folder has downloaded, open the folder and copy the upload folder.
</p>

<p>
<img width="1128" alt="Screen Shot 2023-11-13 at 10 58 03 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/036bdc19-d94c-4850-9f60-eb17817becfd">
</p>

<p>
30. Open the local drive folder (c:), go into the "inetpub" folder, go into the "wwwroot" folder, and paste the "upload" folder.
</p>

<p>
<img width="1127" alt="Screen Shot 2023-11-13 at 11 00 40 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/4e7b643a-c1b2-457e-89b9-207e5add50be">
<img width="1131" alt="Screen Shot 2023-11-13 at 11 02 28 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/bf4b40e8-ce47-42bb-8fb7-d95bd71f79db">
</p>

<p>
31. Once the upload folder has been copied over, rename the "upload" folder to "osTicket"  
</p>

<p>
<img width="1124" alt="Screen Shot 2023-11-13 at 11 12 20 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/04eceb69-ae43-4943-b57b-fb9377518793">
</p>

<p>
32. Go back to IIS and restart the server again. (repeat step 28)
</p>

<p>
33. Inside IIS click on the drop down arrow for "sites", click on the drop down arrow for "default web site", click on "osTicket", and on the right side of the screen click on "browse *.80(http)". This should bring you to a webpage for osTicket installer.
</p>

<p>
<img width="1242" alt="Screen Shot 2023-11-13 at 11 20 59 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/7da45e6b-15c3-4ccd-b263-54457a2a649f">
<img width="1440" alt="Screen Shot 2023-11-13 at 11 23 36 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/518ef0ae-e669-401a-ac5f-d3569db3e3e7">
</p>










