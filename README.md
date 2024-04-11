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

1.Make Azure Account

2. Create Azure VM-windows 10, 4vCPUs
   
3. Enable IIS with CGI & Common HTTP features
- World Wide Web Services -> Application Development Features ->
  
[X] CGI

[X] Common HTTP Features
4 Enable IIS Management console
- Internet Information Services -> Web Management Tools -> IIS Management Console
  
	[X] IIS Management Console
5. Install PHP manager for IIS
6. Install Rewrite Module
  
7.Create the directory C:\PHP

8. Install PHP 7.3.8 & unzip the contents into C:\PHP
   
9.Download and Install VC redist.x86.exe

10. Download and install MYSQL
 - Typical Setup ->
-Launch Configuration Wizard (after install) ->
-Standard Configuration ->
-create password
11. Open ISS as an Admin      
  -   Register PHP from within IIS
  - Reload IIS (Open IIS, Stop and Start the server)
    
12.Install osTicket v1.15.8
- Download osTicket from the Installation Files Folder
- Extract and copy “upload” folder to c:\inetpub\wwwroot
- Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
  
13. Reload IIS (Open IIS, Stop and Start the server)
Go to sites -> Default -> osTicket
- On the right, click “Browse *:80”
  
14. Go back to IIS, sites -> Default -> osTicket
- Double-click PHP Manager
- Click “Enable or disable an extension”
- Enable: php_imap.dll
- Enable: php_intl.dll
- Enable: php_opcache.dll
- Refresh the osTicket site in your browse, observe the changes
  
15. Rename: ost-config.php
- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
  
16.  Assign Permissions: ost-config.php
- Disable inheritance -> Remove All
- New Permissions -> Everyone -> All

17.   Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)

18. From the Installation Files, download and install HeidiSQL.
- Open Heidi SQL
- Create a new session, root/Password1
- Connect to the session
- Create a database called “osTicket”

19. Continue Setting up osticket in the browser
MySQL Database: 
MySQL Username: 
MySQL Password: 
Click “Install Now!”

20. Browse to your help desk login page: http://localhost/osTicket/scp/login.php

21. Clean up
- Delete: C:\inetpub\wwwroot\osTicket\setup
- Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/6jOCfyD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I have created the Azure account. I'm creating the Azure VM which is using Windows 10 and has 4vCPU's.When you choose your VM, it is automatically going to give you a Vnet to go along with it.After this step you would go to the networking tab to check everything. The final step is to click review and create.</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
