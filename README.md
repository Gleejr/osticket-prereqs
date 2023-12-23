<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This comprehensive tutorial provides an in-depth exploration of the prerequisites and step-by-step installation process for osTicket, an open-source help desk ticketing system. Before delving into the installation procedure, it thoroughly discusses the necessary prerequisites, ensuring a clear understanding of the underlying requirements for a successful setup. The tutorial then proceeds to guide users through each stage of the installation, offering detailed insights into the configuration options and key settings involved in deploying osTicket effectively. By elaborating on the installation process, this tutorial aims to equip users with a comprehensive understanding of how to seamlessly integrate and utilize osTicket for efficient help desk management.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation Steps</h2>

<p>
1. In the Azure portal, enter 'Resource Groups' in the search bar above, and then select the 'Resource Groups' option.
</p>

<p>
  
  ![2023-11-07_20-25-09](https://github.com/Gleejr/Configure-ad/assets/148407820/7cc33271-8449-4308-807e-c30cb75d85a6) 
</p>


<p>
2. Select 'Create' to initiate the creation of a new resource group.
</p>
  <p>
  
  ![image](https://github.com/Gleejr/Configure-ad/assets/148407820/12f10b7d-3861-4515-932b-ef475d904c35)
</p>


<p>
3. Enter 'OsTicket-Lab' for the resource group and choose 'West US 3' as the region. Click on 'Review + Create' and then proceed to click 'Create' once more."
</p>
 
<p>
  <img width="781" alt="Screen Shot 2023-11-12 at 10 09 12 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/00cc4f18-92f7-44fa-9f9e-184dc9d1a4bf">
</p>


<p>
4. After creating the resource group, enter 'Virtual Machines' into the search bar above and proceed to select 'Virtual Machines.'
</p>

<p>
 <img width="888" alt="Screen Shot 2023-11-07 at 8 46 03 PM" src="https://github.com/Gleejr/Configure-ad/assets/148407820/504f8572-b736-4ef7-8b51-4b23baf6b49e">
</p>


<p>
5. Click on 'Create a virtual machine hosted by Azure.' 
</p>

<p>
  <img width="622" alt="Screen Shot 2023-11-07 at 8 50 42 PM" src="https://github.com/Gleejr/Configure-ad/assets/148407820/650e51a1-27dd-436d-adb8-37db85bbc6bb">
</p>


<p>
6. Choose 'OsTicket-Lab' as the resource group created in step 2. Enter 'VM1' as the virtual machine name, select 'West US 3' as the region, and choose the 'Windows 10 Pro' image.
</p>

<p>
  <img width="772" alt="Screen Shot 2023-11-12 at 10 15 38 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/27099087-ce65-4b7c-b63a-f6ca18fbdaae">
</p>


<p>
7. Choose the 'Standard_D4s_v3 - 4 vCPUs 16 GiB memory' size. Set 'labuser' as the username and 'Password1234' as the password.
</p>

<p>
  <img width="772" alt="Screen Shot 2023-11-12 at 10 18 30 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/1ff037b8-2971-48fb-930e-847e3e9821b4">
</p>


<p>
8. Click on 'Review + Create,' then proceed to click 'Create' for the first virtual machine (VM-1).
</p>

<p>
  <img width="282" alt="Screen Shot 2023-11-07 at 9 20 18 PM" src="https://github.com/Gleejr/Configure-ad/assets/148407820/edbeace0-962d-4353-b7d2-ebc042b7cb01">
  <img width="363" alt="Screen Shot 2023-11-07 at 9 22 01 PM" src="https://github.com/Gleejr/Configure-ad/assets/148407820/d98e55e4-cca2-43c8-91a9-1024c243600f">
</p>

<p>
9. Go to 'Virtual Machines,' navigate into 'VM1,' and retrieve the public IP address.
</p>

<p>
  <img width="1291" alt="Screen Shot 2023-11-12 at 10 27 32 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/b7b24d9d-b47e-4de4-a4bb-36f4075d4cec">
</p>


<p>
10. Launch Remote Desktop and log in to VM1 using the username and password set in step 7.
</p>

<p>
  <img width="711" alt="Screen Shot 2023-11-12 at 10 30 21 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/cb4fd3f5-d8d7-4518-a0f9-0aae864455d2">
  <img width="662" alt="Screen Shot 2023-11-12 at 10 30 47 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/22a3b02f-c2e0-4b47-8f22-8c0f194677f5">
</p>


<p>
11. Right-click on the Windows icon, select 'Run,' and type in 'control.' 
</p>

<p>
  <img width="436" alt="Screen Shot 2023-11-12 at 10 41 03 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/23a04e74-7154-408b-b60c-3e87149a9136">
</p>

<p>
12. Click on 'Programs' and then select 'Turn Windows features on and off.'
</p>

<p>
  <img width="651" alt="Screen Shot 2023-11-12 at 10 45 57 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/8a577b33-f24a-4e95-87dd-e55f9bc96898">
  <img width="527" alt="Screen Shot 2023-11-12 at 10 45 04 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/23de8513-ce01-472b-9f66-bfc05fb086f3">
</p>


<p>
13. Click on 'Internet Information Services,' expand it, then expand 'World Wide Web Services,' expand 'Application Development Features,' and check the box next to 'CGI.'
</p>

<p>
  <img width="418" alt="Screen Shot 2023-11-12 at 10 49 28 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/c1d42803-707e-4e53-89ab-4d7efa4bd2ee">
  <img width="427" alt="Screen Shot 2023-11-12 at 10 50 34 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/5db8ae3b-f1fb-44ad-8b24-66a9f0a1fc13">
  <img width="416" alt="Screen Shot 2023-11-12 at 10 51 26 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/6ea5ed8d-6708-453d-80eb-eb518db2b7fd">
  <img width="406" alt="Screen Shot 2023-11-12 at 10 52 13 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/bd05881d-a6e7-45f4-b51d-e56d0668fd57">
</p>

<p>
14. Expand 'Common HTTP Features' and ensure that every box is checked. Click OK, and the installation will start.
</p>

<p>
  <img width="418" alt="Screen Shot 2023-11-13 at 8 51 29 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/dde4e3d3-66d4-4021-85ff-f0d49c1ca333">
  <img width="659" alt="Screen Shot 2023-11-13 at 8 51 59 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/4f5ba23d-516a-48bf-97cf-e0240105d84f">
</p>

<p>
15. Once the installation has completed, open a web browser and type in 127.0.0.1. This can test if the web server is working by populating the default IIS website.
</p>

<p>
  <img width="724" alt="Screen Shot 2023-11-13 at 8 58 51 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/dcd410a0-11d8-4a97-a64d-cf16b40b839a">
</p>

<h3>Install PHP Manager for IIS</h3>

<p>
16. Download PHP Manager for IIS. Once the download is complete, click 'Next,' 'I Agree,' and then 'Next' again. After it has successfully installed, click 'Close.'
</p>

<p>
<img width="505" alt="Screen Shot 2023-11-13 at 9 07 57 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/29e09e0e-85b9-444c-a3cd-7ba6a037e721">
</p>

<h3>Install Rewrite Module</h3>

<p>
17. Download the Rewrite Module. Once the download is complete, select 'I agree' and click 'Install.' After it has successfully installed, click 'Close.'
</p>

<p>
<img width="501" alt="Screen Shot 2023-11-13 at 9 18 59 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/106a29b9-70b2-4b0b-95bb-c880ea5a8952">
</p>

<h3>Create a directory for PHP on the local hard drive & Install PHP 7.3.8</h3>

<p>
18. Open File Explorer, type 'c:' to go to the local drive, and create a new folder named 'PHP.'
</p>

<p>
<img width="1122" alt="Screen Shot 2023-11-13 at 9 27 59 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/49e62e44-da2f-46a5-a60f-e87e5727fc39">
</p>

<p>
19. Download the PHP 7.3.8 zip folder. Once the PHP zip folder has downloaded, right-click and select 'Extract All.' 
</p>

<p>
<img width="1130" alt="Screen Shot 2023-11-13 at 9 39 05 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/9dac114c-2762-44be-8c94-6a6d47874046">
</p>

<p>
20. Select 'Browse' and choose the PHP folder that was created in step 18. 
</p>

<p>
<img width="1130" alt="Screen Shot 2023-11-13 at 9 39 05 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/9dac114c-2762-44be-8c94-6a6d47874046">
</p>

<h3>Install VC_redist.x86</h3>

<p>
21. Download VC_redist.x86. Once the VC_redist.x86 file has downloaded, select 'I agree' and click 'Install.' After it has successfully installed, click 'Close.'
</p>

<p>
<img width="483" alt="Screen Shot 2023-11-13 at 9 54 12 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/9a9efe57-1eb4-43d9-bd19-6f75d77a22e9">  
</p>

<h3>Install MySQL 5.5.62</h3>

<p>
22. Download MySQL 5.5.62. Once the MySQL 5.5.62 file has downloaded, click 'Next,' select 'I agree,' and click 'Next.'
</p>

<p>
<img width="501" alt="Screen Shot 2023-11-13 at 10 01 16 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/9195f2e4-45be-4f50-8b76-711e431572e7">
</p>

<p>
23. Choose 'Typical' for the setup type, click 'Install,' and continue clicking 'Next' until 'Finish' populates.
</p>

<p>
<img width="503" alt="Screen Shot 2023-11-13 at 10 03 53 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/eb821400-fbd5-4ecb-90da-2d29fac2ec67">
</p>

24. Click 'Next,' select 'Standard Configuration,' and continue clicking 'Next' until you reach a screen to create a password.
</p>

<p>
<img width="510" alt="Screen Shot 2023-11-15 at 8 41 12 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/e7ec0850-8429-4c91-af55-a8c1ea82fc08">
</p>

25. Enter 'Password1234' for the password and click 'Next.' Click 'Execute' to begin the installation. Once it has successfully installed, click 'Finish.'
</p>

<p>
<img width="500" alt="Screen Shot 2023-11-13 at 10 13 43 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/55437f9f-3cf1-4ca3-a256-5c23f7107913">
<img width="506" alt="Screen Shot 2023-11-13 at 10 14 44 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/5b8b7c77-d86d-4565-b29d-5de18364d593">
</p>

<h3>IIS Configurations</h3>

<p>
26. Go to the Start menu and type in 'IIS.' Run IIS as an administrator.
</p>

<p>
<img width="1440" alt="Screen Shot 2023-11-13 at 10 21 47 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/0cb553d2-8267-4beb-86df-5b2e6695d160">
</p>

<p>
27.Once IIS opens, double-click on PHP Manager, and click on 'Register new PHP version.'
</p>

<p>
<img width="1258" alt="Screen Shot 2023-11-13 at 10 24 15 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/ffd18dd6-cfac-4b88-96d7-4cd8f24d6c51">
<img width="1254" alt="Screen Shot 2023-11-13 at 10 26 55 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/91b54f41-9471-49ee-959a-db9da86630b8">
</p>

<p>
28. Click on the three dots, find the PHP folder that was created in step 17, select the 'PHP-cgi' file, and press 'OK.'
</p>

<p>
<img width="514" alt="Screen Shot 2023-11-13 at 10 29 48 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/3f48422e-4075-4663-a3c4-9feb4b2e7d20">
<img width="710" alt="Screen Shot 2023-11-13 at 10 33 55 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/4aa603fb-3e02-44ee-8ec7-1e502b4d6ede">
</p>

<p>
29.Go back to the main screen, click on the name of the server (VM1 'VM1/labuser'), and click 'Restart.'
</p>

<p>
<img width="1254" alt="Screen Shot 2023-11-13 at 10 38 27 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/841458ea-4962-4f2f-8718-c31ef1cb22a8">
</p>

<h3>Install OsTicket</h3>
<p>
30. Download the osTicket v1.15.8 zip folder. Once the osTicket zip folder has downloaded, open the folder and copy the 'upload' folder.
</p>

<p>
<img width="1128" alt="Screen Shot 2023-11-13 at 10 58 03 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/036bdc19-d94c-4850-9f60-eb17817becfd">
</p>

<p>
31. Open the local drive folder (C:), navigate to the 'inetpub' folder, go into the 'wwwroot' folder, and paste the 'upload' folder.
</p>

<p>
<img width="1127" alt="Screen Shot 2023-11-13 at 11 00 40 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/4e7b643a-c1b2-457e-89b9-207e5add50be">
<img width="1131" alt="Screen Shot 2023-11-13 at 11 02 28 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/bf4b40e8-ce47-42bb-8fb7-d95bd71f79db">
</p>

<p>
32. Once the 'upload' folder has been copied over, rename the 'upload' folder to 'osTicket.'
</p>

<p>
<img width="1124" alt="Screen Shot 2023-11-13 at 11 12 20 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/04eceb69-ae43-4943-b57b-fb9377518793">
</p>

<p>
33. Go back to IIS and restart the server again (repeat step 28).
</p>

<p>
34. Inside IIS, click on the drop-down arrow for 'Sites,' then click on the drop-down arrow for 'Default Web Site,' further click on 'osTicket,' and on the right side of the screen, click on 'Browse *.80 (HTTP).' This should bring you to a webpage for the osTicket installer.
</p>

<p>
<img width="1242" alt="Screen Shot 2023-11-13 at 11 20 59 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/7da45e6b-15c3-4ccd-b263-54457a2a649f">
<img width="1440" alt="Screen Shot 2023-11-13 at 11 23 36 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/518ef0ae-e669-401a-ac5f-d3569db3e3e7">
</p>

<p>
35. Go back to IIS, click on 'osTicket' again on the left, and double-click on PHP Manager. Click on 'Enable or Disable an Extension.'
</p>

<p>
<img width="1078" alt="Screen Shot 2023-11-15 at 9 51 31 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/574b7c40-7742-4504-be31-5f21e21a24aa">
<img width="1166" alt="Screen Shot 2023-11-15 at 9 53 12 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/553610a1-362f-4630-8247-833955f55078">
</p>

<p>
36. Enable 'php_imap.dll,' 'php_intl.dll,' and 'php_opcache.dll.' Go back to the browser and refresh osTicket. (There should be more green check marks.)
</p>

<p>
<img width="1171" alt="Screen Shot 2023-11-15 at 9 57 24 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/ac3eb1b5-1b5e-4bf0-b2e3-7dba88eccb0d">
<img width="907" alt="Screen Shot 2023-11-15 at 10 01 32 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/329b46a7-fe90-4dc1-8b68-43ec72d46602">
</p>

<p>
37. Go back into File Explorer, navigate to the 'wwwroot' folder (from step 31), then enter the 'osTicket' folder, and finally, enter the 'include' folder.
</p>

<p>
<img width="944" alt="Screen Shot 2023-11-15 at 10 06 54 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/6d15ef4b-696a-4c8a-a988-5f4da8aa682c">
<img width="1106" alt="Screen Shot 2023-11-15 at 10 07 30 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/dd1cabf6-7c51-4283-b846-fddaf2df8503">
</p>

<p>
38. Rename 'ost-sampleconfig.php' to 'ost-config.php.'
</p>

<p>
<img width="901" alt="Screen Shot 2023-11-15 at 10 10 50 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/388563c7-60c8-4b3d-9c9a-da7c2f8d2ee0">
<img width="872" alt="Screen Shot 2023-11-15 at 10 11 52 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/fa2fda26-9c51-424e-aabc-23cbb2c22a52">
</p>

<p>
39. Right-click on this file, select 'Properties,' go to the 'Security' tab, and click on 'Advanced.'
</p>

<p>
<img width="817" alt="Screen Shot 2023-11-15 at 10 14 17 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/394c110f-188b-405e-8811-c5b81eb3365a">
<img width="364" alt="Screen Shot 2023-11-15 at 10 15 26 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/d711f8f3-ce47-498e-83eb-ccae2eb3a63f">
</p>

<p>
40. Click on 'Disable Inheritance' and select 'Remove all inherited permissions from this object.'
</p>

<p>
<img width="763" alt="Screen Shot 2023-11-15 at 10 17 39 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/0aab3188-9158-46e5-b709-e264764bf83f">
<img width="524" alt="Screen Shot 2023-11-15 at 10 19 39 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/369e7f08-b4ed-4d82-a298-ec7c05fdd961">
</p>

<p>
41.Click on 'Add' and then click on 'Select a principal.' Type in 'Everyone,' click on 'Check Names,' and select 'OK.'
</p>

<p>
<img width="770" alt="Screen Shot 2023-11-15 at 10 22 08 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/80b68f28-8ec0-4093-aaa9-d873d5026e43">
<img width="911" alt="Screen Shot 2023-11-15 at 10 23 29 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/8aff067a-6c0c-4ca2-9f87-607b0e8422e5">
<img width="464" alt="Screen Shot 2023-11-15 at 10 24 58 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/214f26e4-0a5a-4410-a475-2caa220d8da8">
</p>

<p>
42. Click on 'Full control,' which will check all the boxes below, and click 'OK.' Click on 'Apply' and 'OK' again.
</p>

<p>
<img width="920" alt="Screen Shot 2023-11-15 at 10 28 48 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/4cbcf795-c655-4b5f-a0fb-5d55cfb58f6e">
</p>

<p>
43. Go back to osTicket in the browser and click 'Continue' at the bottom.
</p>

<p>
<img width="891" alt="Screen Shot 2023-11-15 at 10 33 13 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/b85fa39b-3a71-4ec3-b95e-68c8e806b021">
</p>

<p>
44. Complete the information on the page, including your name, username, password, and email address.
</p>

<p>
<img width="834" alt="Screen Shot 2023-11-15 at 10 37 41 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/9520fc84-823a-45e1-96d2-64480a234e17">
</p>

<h3>Install Heidi SQL</h3>

<p>
45. Download Heidi SQL. Once the Heidi SQL has downloaded, select 'I accept' and continue clicking 'Next' and 'Install' until you reach 'Finish.'
</p>

<p>
<img width="609" alt="Screen Shot 2023-11-15 at 10 41 23 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/ed99e8bb-d061-4e77-8b46-1c743b327838">
</p>

<p>
46. Heidi will launch after the installation. Click 'New,' enter 'Password1234' for the password (this is the password for MySQL that was set up in step 25), and click 'Open' (this will establish a connection to the MySQL server).
</p>

<p>
<img width="692" alt="Screen Shot 2023-11-15 at 10 46 47 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/ad0f27dc-34e8-4ab9-9e7f-d7bc2c5d0284">
<img width="690" alt="Screen Shot 2023-11-15 at 10 47 57 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/f6c18104-14eb-45b2-8303-4ed182de9186">
<img width="690" alt="Screen Shot 2023-11-15 at 10 47 57 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/430ead9c-e5dd-4aac-bc00-121a936c96b7">
</p>

<p>
47. Inside Heidi, right-click on 'Unnamed,' move the cursor to 'Create New,' and select 'Database.' Type in the name 'osTicket' and click 'OK.'
</p>

<p>
<img width="939" alt="Screen Shot 2023-11-15 at 10 54 46 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/12ea83da-abf9-47c2-aa87-7aea27d93261">
<img width="321" alt="Screen Shot 2023-11-15 at 10 58 00 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/4c049a33-a151-4579-aa39-02dfb7d3491a">
</p>

<p>
48. Enter the MySQL Database: 'osTicket,' MySQL Username: 'root,' and MySQL Password: 'Password1234.' Click 'Install Now,' and osTicket should install onto this server.
</p>

<p>
<img width="675" alt="Screen Shot 2023-11-15 at 10 59 36 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/c0afaacb-c45f-447a-b23e-c34bb1afe12b">
<img width="973" alt="Screen Shot 2023-11-15 at 11 02 30 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/79ddd2e0-9eee-4068-b22a-277dc71f1c77">
</p>

<p>
49. Once fully installed, you will see a 'Congratulations' message."
</p>

<p>
<img width="947" alt="Screen Shot 2023-11-15 at 11 03 16 PM" src="https://github.com/Gleejr/osticket-prereqs/assets/148407820/634496ed-f3ea-4ffc-b193-3d39546c198e">
</p>



















