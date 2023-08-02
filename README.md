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
