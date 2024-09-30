<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

-https://www.youtube.com/watch?v=w44PZBRPqsY

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable Internet Information Services
- Install Web Platform Installer
- Install My Sequel/Set-up Username and Password
- Install C++ Resdistributable
- Configure Permissions and Install OS Ticket

<h2>Installation Steps</h2>

<p>


</p>
<p>


Step 1: We can do a quick search for Virtual Machine and as we create the virtual machine, we will have the option to create the Resource Group. Here we select Create New to name the name the Resource Group 'RG-osTicket' and build out the Virtual Machine (VM)
![image](https://github.com/user-attachments/assets/bb702d7e-9fd0-4640-99ee-231af213c9db)

 Connect Virtual Machine with Remote Desktop using the VM's public IP address
   ![68747470733a2f2f692e696d6775722e636f6d2f44474f577253352e706e67](https://github.com/user-attachments/assets/d05f25f8-62f7-41ca-bbf8-8163e2d6389b)
    
To connect to the virtual machine, we search on the local machine for 'Remote Desktop Connection' and the following window opens and you can now copy and paste the public IP address into the provided space. Then press the Connect button.
![68747470733a2f2f692e696d6775722e636f6d2f303661663479482e706e67](https://github.com/user-attachments/assets/eb42a95f-2fb9-4149-8581-7aa4e57d4fa8)
Once you are connected and inside the virtual machine we will need to install the Web Platform Installer. To install the Web Platform Installer we will search for the Control Panel --> under programs select Uninstall a Program.
![68747470733a2f2f692e696d6775722e636f6d2f596c5a6c7736432e706e67](https://github.com/user-attachments/assets/e98823ce-0d4b-4fef-b025-dcb516a9a68e)
After we've reached the next page, we can now select to Turn Windows features on or off --> then enable the 'Internet Information Services' (IIS) from the available services.
![68747470733a2f2f692e696d6775722e636f6d2f585951516c70612e706e67 (1)](https://github.com/user-attachments/assets/bbb1335e-3349-4eaa-b245-c98a22095786)
Now we can download and install Web Platform Installers. Web Platform Installers (WebPI) provides a simplified installation workflow for installing common open source web applications and web platform technologies.
![68747470733a2f2f692e696d6775722e636f6d2f353946533353342e706e67](https://github.com/user-attachments/assets/35218e09-1443-440f-8a8c-3b7c9aa51fcb)
Once WebPI is installed, we can now add MySQL 5.5 database, PHP 5.6.31, and the various verisons of between PHP (x86) 7.0 and 7.3.
![68747470733a2f2f692e696d6775722e636f6d2f537748596d74372e706e67](https://github.com/user-attachments/assets/93db641e-c8f5-40a3-9dae-5f4db499ae81)
MySQL 5.5 will require a name and password, root and Password1 respectively when you try to install. Make note of the name / password in a text file as you will need it again later on in the installation process.
![68747470733a2f2f692e696d6775722e636f6d2f494946435250472e706e67](https://github.com/user-attachments/assets/d97711c5-3de4-434b-b3c3-daa337c9a963)
From the downloaded files, we can now install and extract the osTicket file. Extract and copy the “upload” folder INTO c:\inetpub\wwwroot 3. Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
![68747470733a2f2f692e696d6775722e636f6d2f46317750474c312e706e67](https://github.com/user-attachments/assets/4720c559-f0c1-4ace-85ff-a94a6a36d21b)
-Reload IIS (Open IIS, Restart the server)** 1. Go to sites -> Default -> osTicket 2. On the right, click Browse *:80
![68747470733a2f2f692e696d6775722e636f6d2f41384c426847532e706e67](https://github.com/user-attachments/assets/3b11894b-cf8f-424a-ae21-dbcfdf1abcbf)
Once browse: 80 is selected a browser window will open presenting osTicket installer page along with the recommendation/prerequisites of use.
Next we'll go back to IIS, sites -> Default -> 1. osTicket 2. Double-click PHP Manager 3. Click Enable or disable an extension 1. Enable: php_imap.dll 2. Enable: php_intl.dll 3. Enable: php_opcache.dll -
![image](https://github.com/user-attachments/assets/6ca0e641-3619-427e-add8-45d7860839a3)
![68747470733a2f2f692e696d6775722e636f6d2f634d74437561412e706e67](https://github.com/user-attachments/assets/53ab4d75-6ce3-4850-a225-5917db48824e)

Refresh the osTicket site in your browser to see what has changed after enabling the PHP extensions
![68747470733a2f2f692e696d6775722e636f6d2f50504e7a6956352e706e67](https://github.com/user-attachments/assets/89282569-b170-49e3-b8ae-aa038a40872d)

Rename: From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php ---> To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
![68747470733a2f2f692e696d6775722e636f6d2f753062437244432e706e67](https://github.com/user-attachments/assets/9774c825-93ae-4a75-8034-62b7473364fd)

Assign Permissions: ost-config.php To change the permissions, right-click ost-config --> select 'properties' --> select the 'Security' tab at the top --> select the 'Advanced' button1. Disable inheritance -> Remove All 2. New Permissions -> Everyone -> All
![68747470733a2f2f692e696d6775722e636f6d2f4473384a5576742e706e67](https://github.com/user-attachments/assets/f2776df5-65c6-4c75-b067-6574044a60dc)
![68747470733a2f2f692e696d6775722e636f6d2f724b6863486b572e706e67](https://github.com/user-attachments/assets/2f9384a2-755c-4da0-acac-53341c3a87c5)
![68747470733a2f2f692e696d6775722e636f6d2f78616a6a50474b2e706e67](https://github.com/user-attachments/assets/30669ad2-4467-450b-aa00-d2112035906f)

Then add new permissions for everyone and give Full Control.
![68747470733a2f2f692e696d6775722e636f6d2f513958514c586d2e706e67](https://github.com/user-attachments/assets/a16e1650-6c65-4ea9-96aa-0484f56dfe94)

After returning to the browser windows with osTicket installer and press 'Continue', you will now see the below form to complete before continuing.
![68747470733a2f2f692e696d6775722e636f6d2f666a4b4167476b2e706e67](https://github.com/user-attachments/assets/50d08c15-2fd7-49bc-b5c2-1cb9665082ed)

Download and install HeidiSQL from Google Drive using the provided defaults that are available in the install wizard.
![68747470733a2f2f692e696d6775722e636f6d2f6f496d773577302e706e67](https://github.com/user-attachments/assets/acf4093b-92fc-4193-a218-ebb957bc5c28)

Next we will do the following in HeidiSql:
Create a new session, username:root/password:Password1
Connect to the session
Create a database called “osTicket”
![68747470733a2f2f692e696d6775722e636f6d2f443251664d45622e706e67](https://github.com/user-attachments/assets/4e1af0ac-4bc7-476b-afd3-16741ea00343)
![68747470733a2f2f692e696d6775722e636f6d2f33624d4850324b2e706e67](https://github.com/user-attachments/assets/3c5b650e-0e72-41b3-99e8-49355d3fa593)
After the database is created, we can now enter those details into osTicket Installer

MySQL Username: root
MySQL Password: Password1
Click “Install Now!”
![68747470733a2f2f692e696d6775722e636f6d2f563347537676542e706e67](https://github.com/user-attachments/assets/6e08ddf8-4f40-45eb-afc8-9a6e4f772cfd)
Results below are from of choosing for "Your Staff Control Panel" or "Your osTicket URL:"
![68747470733a2f2f692e696d6775722e636f6d2f4c6854674939322e706e67](https://github.com/user-attachments/assets/82c20c6b-1fe6-48f3-be6e-7bd3ab91434e)
![68747470733a2f2f692e696d6775722e636f6d2f6a4e6b505a4e432e6a7067](https://github.com/user-attachments/assets/dfd48d1a-f6fc-4f05-aeac-4c4b7200fe62)
"Your osTicket URL" will direct us to the "End User" Portal where Users can submit tickets for assistance from the help desk.
![68747470733a2f2f692e696d6775722e636f6d2f457276624367362e706e67](https://github.com/user-attachments/assets/af2af845-9a66-4a11-8639-b204c081291b)

Clean up

Delete: C:\inetpub\wwwroot\osTicket\setup
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
Login to the osTicket Admin Panel ([http://localhost/osTicket/scp/login.php](http://localhost/osTicket/scp/login.php))
![68747470733a2f2f692e696d6775722e636f6d2f5847487a336c782e706e67](https://github.com/user-attachments/assets/1621b4df-a25f-46f4-bd64-5e0e7b4bfb44)
Set Permission to "Read" only can be acheived by choosing to right-click on 'ost-config.php' --> select properties --> select the 'Security' tab near the top --> then click the 'Advanced' button (not pictured below) --> once advanced settings is selected, you can now select the 'Everyone' principle and now we can select to choose 'Read' only as the preferred permission(s)
![68747470733a2f2f692e696d6775722e636f6d2f4158434965514e2e706e67](https://github.com/user-attachments/assets/e7294df0-e354-48a2-9ba7-2089ffeb9af0)
![68747470733a2f2f692e696d6775722e636f6d2f52313172494d642e706e67](https://github.com/user-attachments/assets/02f4bdce-428f-44df-a940-49fc1bc998bf)














