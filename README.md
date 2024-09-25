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
<img width="341" alt="Screenshot 2024-09-25 103803" src="https://github.com/user-attachments/assets/392efcbb-615b-45f2-9083-7514cfaae9cc">
           1) Install / Enable IIS in Windows WITH CGI. All From the “osTicket-Installation-Files” folder 2)Install PHP Manager for IIS, 3)Install the Rewrite Module, 4)Install My SQL Then unzip PHP into the “C:\PHP” folder. You will use all the files in this folder to install osTicket and some of the dependencies.
 

</p>
<br />

<p>
<img width="433" alt="php project portion" src="https://github.com/user-attachments/assets/77a82b36-9bfc-4833-a020-ba383cebdbba">
1)Open IIS as an Admin. 2)Register PHP from within IIS 3)Reload IIS (Open IIS, Stop and Start the server) 4)Install osTicket v1.15.8 From the “osTicket InstallationFiles”folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot” Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket” 
           5) Reload IIS (Open IIS, Stop and Start the server) 6)Go to sites -> Default -> osTicket On the right, click “Browse *:80”  7)Go back to IIS, sites -> Default -> osTicket  8) Double-click PHP Manager, Click “Enable or disable an extension” -Enable the following: (php_imap.dll) (php_intl.dll) (php_opcache.dll) Refresh the osTicket site in your browser, observe the changes.











</p>
<p>
.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
