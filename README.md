<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
A walkthrough of installing an open source ticketing system, osTicket, in a Microsoft Azure virtual machine. This walkthrough includes all of the prerequisits needed for a succesfful installlation.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Broad Concepts</h2>

-  Set up Azure virtual machines.
-  Set up Internet Information Services.
-  Install prerequisite software.
-  Install osTicket.
-  Configure osTicket. 

<h2>Installation Steps</h2>

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/29222075-8b28-4107-bfa9-798ba4a8679b)

</p>
<p>
We will be setting up osTicket on an Azure virtual machine (VM) for this walkthrough. To start, launch Microsoft Azure, and create a new virtual machine.    
</p>
<br />

<p>

  ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/576fce03-13dc-41dc-8ec7-ac00b55696df)

</p>
<p>
Create a new resource group and name the virtual machine. Select a Windows 10 image and set the number of vcpus to 2 at a minimum. Create a username and password. Click "review + create."  
</p>
<br />

<p>

  ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/3b8aba71-2976-47f8-baf1-47104a5d9e01)

</p>
<p>
If there are no errors, click "create."
</p>
<br />

<p>

  ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/d48d76d0-b7d3-48d3-b6d9-ed9bdc7f1d0f)

</p>
<p>
After the resource group has completed deployment, we need to remote into the newly create Windows VM. Start by selecting your VM. 
</p>
<br />

<p>

  ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/ce14ffc4-3d5e-45e2-9ef8-6912a2f26a59)

</p>
<p>
Copy the VM's public IP address. 
</p>
<br />

<p>

  ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/04e1adec-0644-4ce8-a764-1df4094b1353)

</p>
<p>
Open "Remote Desktop Connection" and paste the VM's public IP address. Click "Connect."
</p>
<br />

<p>

  ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/18a74563-f542-4e67-b39d-3b48f805bf40)

</p>
<p>
Enter the VM's login information. Click "Okay."
</p>
<br />

<p>

  ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/1b00e407-af16-4238-993f-3e32ebc6b971)

</p>
<p>
Once inside the virtual desktop, we will need to install and enable IIS (Internet Information Services). This will allow us to host our instance of osTicket. 
Open up the Control Panel.
</p>
<br />

<p>

  ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/e28aead7-2e0b-4de5-bb94-fe5fa2471fec)

</p>
<p>
Select "Programs."
</p>
<br />

<p>

  ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/a0d246d3-b496-4260-bd64-13cb67fbb5f6)

</p>
<p>
Select "Turn Windows features on or off."
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/1066b547-8ba6-4b6b-80c7-1cb273efb2e2)

</p>
<p>
Inside the directory tree, check the box for "Internet Information Services." Expand "Application Development Features." Check the box for "CGI."
Expand "Common HTTP Features. Check all of the boxes within "Common HTTP Features." Select "OK." Allow Windows to install the changes. 
</p>
<br />
<h2></h2>
Use the following link to access the software needed to run osTicket:

[Installation Files](https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)

</p>
<br />
<h2></h2>
<p>

  ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/b174b565-d23e-4b54-a049-a1842ede3903)

  ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/5440f4ea-42f3-47bc-a160-eb347741ae89)

</p>
<p>
Download and install "PHPManagerForIIS_V1.5.0.msi" from Installation Files.  
</p>
<br />

<p>

  ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/5d63fc22-b0e6-4b52-bd7d-fb363b6af7f9)

  ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/c06439d0-3ca2-4ead-8db3-e5b71e0a7ccf)

</p>
<p>
Download and install "rewrite_amd64_en-US.msi" from Installation Files.  
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/b754d342-407a-4941-af3c-f11dba21b03e)

</p>
<p>
While files are installing, create a new folder im the Windows (C:) root directory labled "PHP."  
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/f0a8a775-1a33-4970-9d53-896978a4fabd)

</p>
<p>
Download "php- 7.3.8-nts-Win32-VC15-x86" from Installation Files.  
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/e0cc7ff7-1803-4eaf-9f96-1fb5d0b4a8de)

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/054c81fa-3bea-479b-abc2-28fb9245fa45)

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/221fce46-e001-423c-81b1-66aa91d4dd62)

</p>
<p>
Extract "php- 7.3.8-nts-Win32-VC15-x86" to C:\PHP  
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/f9c4849a-7ab7-4fd0-8988-b102ca45ab1d)

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/cd092b3f-a29e-486c-9f63-36ae388dce2c)

</p>
<p>
Download and Install "VC_redist.x86.exe" from Installation Files.  
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/89b4f7b2-f55f-4ccc-9892-2abf31d069cc)

</p>
<p>
Download "mysql-5.5.62-win32.msi" from Installation Files.  
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/8b59970e-6a96-4e7e-ae58-8aeafa41f97e)

</p>
<p>
Start the setup by selecting "Typical."  
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/aa944833-20ba-4f57-bbb2-6bedbe51f837)

</p>
<p>
Click "Install."  
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/2217e536-8328-4059-a761-917c4d8cf75d)

</p>
<p>
Check the box to launch the Configuration Wizard. Click "Finish."  
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/e2a8d7d2-82ee-45bc-a98f-de4192b35a00)

</p>
<p>
Select "Standard Configuration."  
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/2d7f3296-d204-4f04-9582-3bbecd65c0e0)

</p>
<p>
Enter your desired root password. Select "Next." 
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/4732a1b2-218f-4afb-b2f2-aa9618f4cacb)

</p>
<p>
Select "Execute."
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/147ec3bd-8d52-4722-b8d0-e207caf8fea2)

</p>
<p>
Once configuration is complete, select "Finish."
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/52365348-2cc8-4af7-87c0-c4d528eb4617)

</p>
<p>
After files have been installed, open Internet Information Services (IIS) and run as administrator. 
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/38a070a7-f47c-4ecf-b20b-e028c7ee66f9)

</p>
<p>
Select "PHP Manager." 
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/66b7928e-24db-442a-8aeb-6a321e25d0c0)

</p>
<p>
Select "Register new PHP version." 
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/75003c16-1a10-47ae-b75e-1c6d6318f864)

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/27443480-4b86-4ed0-bc0d-f234c741cfce)

</p>
<p>
Select C:\PHP\php-cgi as the executable file. Select Okay.
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/6fe5e6df-a892-43f5-ba4b-0fc6a5eb44f3)

</p>
<p>
Restart IIS. 
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/6074cb8e-6066-4ad0-92b7-95d6edf17322)

</p>
<p>
Download "osTicket-v1.15.8.zip" from Installation Files.  
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/50dc08b6-634d-4b0d-bac3-91a53d98b958)

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/bc84a6fa-b25d-403a-b371-00f56651936a)

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/339928cc-9f32-4285-bf1b-bb17a08e2ca8)

</p>
<p>
Make a copy of the "upload" folder and paste it in C:\inetpub\wwwroot. 
Rename "upload" to "osTicket"
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/0b1e8681-b529-4389-bf54-707392fc8a13)

</p>
<p>
Restart IIS.  
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/3a62edbe-37b2-4e85-ba40-94c038cfc77d)

</p>
<p>
On the left-hand side of IIS go to sites->Default->osTicket. Select "Browse *:80(http)"   
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/56264314-8d27-42bc-98a6-6cab9dc1472f)

</p>
<p>
You should see this page. some extensions are missing. We will need to enable them.    
</p>
<br />

<p>

 ![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/19dced79-f457-48e3-92d5-ae97c2dae18f)

</p>
<p>
Select PHP Manager in IIS.     
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/b649a9ae-85f9-433b-a329-182ecdef7197)

</p>
<p>
Select "Enable or disable an extension."     
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/76ef4464-942f-422b-8555-5eefe50fd64e)

</p>
<p>
Right-click and enable php_imap.dll, php_intl.dll, php_opcache.dll     
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/fcbef2f9-06bc-45e2-9fb8-b5ad90a9bef3)

</p>
<p>
Now "Browse *:80(http)" should look like this. (Do not click Continue just yet)       
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/63dd9584-457c-4d80-ab6f-c819cfb41a7e)

</p>
<p>
Go to C:\inetpub\wwwroot\osTicket\include and rename "ost-sampleconfig.php" to "ost-config.php"       
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/8247f3ac-3435-4dd9-86b8-f7f4546ccff7)

</p>
<p>
Now we need to assign permissions to "ost-config.php." Right-click "ost-config.php" and select "Properties."       
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/0fefbe3a-15d0-4679-b677-2042f060b9be)

</p>
<p>
Select "Advanced."       
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/2553bb4c-3a1e-4064-b92f-85e6232dc6b9)

</p>
<p>
Select "Disable inheritance."       
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/34335dcc-def3-4c32-bd8f-6bbbf282edf2)

</p>
<p>
Select "Remove all inherited permissions from this object."       
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/dedc18a8-63f2-4f80-ab07-03e998cc1b51)

</p>
<p>
Now add a new inheritance.        
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/bfb62e44-9b40-4db1-a13d-1dcd6a7e958e)

</p>
<p>
Select a principal.         
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/868583f5-b4af-4e86-b8bf-b07ab5ac23ea)

</p>
<p>
Assign inheritance to Everyone.         
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/f56082a6-8a80-415f-84fd-cde81f17a520)

</p>
<p>
Check the box for "Full control."         
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/afd39325-39ac-48f2-b601-0796f10b8e65)

</p>
<p>
Select "Apply."         
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/2c7144d3-b832-4f44-a3ae-ac480101319f)

</p>
<p>
Go back to the osTicket site and select "Continue."        
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/755cd7b7-3e70-4a04-86a8-98dd843d8d05)

</p>
<p>
Fill out the form with the relevant information. DO NOT FILL OUT DATABASE SETTINGS JUST YET!        
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/11408fa9-af9e-45e6-b28d-6492ce9344db)

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/f68999c9-be12-4963-8478-457938ed6f78)

</p>
<p>
Download and install "HeidiSQL_12.3.0.6589_Setup.exe" Launch HeidiSQL after installation.          
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/11308ddc-8d67-48cd-8270-d1541629f15e)

</p>
<p>
Create a new session inside HeidiSQL.        
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/a348a006-b922-4395-87a8-f7fe45c55239)

</p>
<p>
Assign a username and password and click "Open"        
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/4ab34a1d-65b0-4e6e-b704-88756bb6effa)

</p>
<p>
On the left-hand side, right-click and create a new database called "osTicket."        
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/e2cf06b6-9aa8-474e-aa88-3a3f05c5db97)

</p>
<p>
Back in the osTicket installer, fill out the Database settings. Click "Install Now."        
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/f50d02ba-349f-4f10-8568-a6d786e90f51)

</p>
<p>
If you reach this screen, congratulations!! you have successfully installed osTicket!       
</p>
<br />
<h2>Post-Install Clean Up</h2>

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/a95ad35b-8262-4917-92da-edf848737dc8)

</p>
<p>
Delete the "setup" folder in C:\inetpub\wwwroot\osTicket        
</p>
<br />

<p>

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/086e680d-2aa4-4afd-a037-3905de7496f2)

![image](https://github.com/Josh-arendt/osTicket_Prereqs_Installation/assets/140751318/7f0df95e-27e3-4f7a-894a-ae30b30619a0)

</p>
<p>
Set C:\inetpub\wwwroot\osTicket\include\ost-config.php to "Read Only."        
</p>
<br />

<h2>End of Tutorial</h2>
















