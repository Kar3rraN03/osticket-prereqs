<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>
   
1. Enable IIS with CGI & Common HTTP features
- World Wide Web Services -> Application Development Features ->
  
[X] CGI

[X] Common HTTP Features
2. Enable IIS Management console
- Internet Information Services -> Web Management Tools -> IIS Management Console
  
	[X] IIS Management Console
3. Install PHP manager for IIS
4. Install Rewrite Module
  
5.Create the directory C:\PHP

6. Install PHP 7.3.8 & unzip the contents into C:\PHP
   
7.Download and Install VC redist.x86.exe

8. Download and install MYSQL
 - Typical Setup ->
-Launch Configuration Wizard (after install) ->
-Standard Configuration ->
-create password
9. Open ISS as an Admin      
  -   Register PHP from within IIS
  - Reload IIS (Open IIS, Stop and Start the server)
    
10.Install osTicket v1.15.8
- Download osTicket from the Installation Files Folder
- Extract and copy “upload” folder to c:\inetpub\wwwroot
- Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
  
11. Reload IIS (Open IIS, Stop and Start the server)
Go to sites -> Default -> osTicket
- On the right, click “Browse *:80”
  
12. Go back to IIS, sites -> Default -> osTicket
- Double-click PHP Manager
- Click “Enable or disable an extension”
- Enable: php_imap.dll
- Enable: php_intl.dll
- Enable: php_opcache.dll
- Refresh the osTicket site in your browse, observe the changes
  
13. Rename: ost-config.php
- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
  
14.  Assign Permissions: ost-config.php
- Disable inheritance -> Remove All
- New Permissions -> Everyone -> All

15.   Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)

16. From the Installation Files, download and install HeidiSQL.
- Open Heidi SQL
- Create a new session, root/Password1
- Connect to the session
- Create a database called “osTicket”

17. Continue Setting up osticket in the browser
MySQL Database: 
MySQL Username: 
MySQL Password: 
Click “Install Now!”

18. Browse to your help desk login page: http://localhost/osTicket/scp/login.php

19. Clean up
- Delete: C:\inetpub\wwwroot\osTicket\setup
- Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/c0N7PKo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Before enabling IIS in windows; you have to access the control panel.Next step is to go programs and press turn windows features on or off. Then start enabling CGI and Common HTTP Features in your Azure Virtual Machine settings. Navigate to World Wide Web Services, then Application Development Features, and check the boxes for CGI and Common HTTP Features. </p>
<br />

<p>
<img src="https://i.imgur.com/0AjqU8E.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Ensure that the IIS Management Console is checked under Internet Information Services under Web Management Tools.
</p>
<br />

<img src="https://i.imgur.com/mvrawj7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install PHP Manager for IIS from the installation files (PHPManagerForIIS_V1.5.0.msi) on Azure VM.

</p>
<br />

</p>
<img src="https://i.imgur.com/rDsf13E.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Similarly, download and install the Rewrite Module (rewrite_amd64_en-US.msi) for IIS.
<br />

</p>
<img src="https://i.imgur.com/ImNykgv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a directory C:\PHP 
<br />

</p>
<img src="https://i.imgur.com/Kiz5Jfo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
 Unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into this C:\PHP directory. If prompted, choose "Keep" for any file download warnings. If downloading PHP 7.3.8 is problematic, try using Google Chrome. </p><br />

 </p>
<img src="https://i.imgur.com/LA1EcOx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Install VC_redist.x86.exe from the installation files.
<br />

 </p>
<img src="https://i.imgur.com/nWpM57L.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/F8QqQ0B.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
</p>
Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi) on your Azure VM. During installation, choose the Typical Setup option and set the MySQL root password as ypur chosen password.
<br />

 </p>
<img src="https://i.imgur.com/QfnN0Co.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Open IIS as an Administrator, register PHP within IIS, and reload IIS by stopping and starting the server.<br />

 </p>
<img src="https://i.imgur.com/tDxZq8V.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Download osTicket from the Installation Files folder, extract the contents, and copy the "upload" folder to C:\inetpub\wwwroot. Rename the "upload" folder to "osTicket".
<br />

</p>
<img src="https://i.imgur.com/S592idO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p> In IIS, navigate to the osTicket site, double-click PHP Manager, and enable the extensions php_imap.dll, php_intl.dll, and php_opcache.dll. Refresh the osTicket site in your browser.
<br />


</p>
<img src="https://i.imgur.com/3Hbh9fA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Y48pitn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />Rename ost-sampleconfig.php to ost-config.php in C:\inetpub\wwwroot\osTicket\include, and assign permissions to ost-config.php: Disable inheritance, remove all permissions, and add permissions for Everyone with full control..


</p>
<img src="https://i.imgur.com/jWBezvS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/EciTsPb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p> Install HeidiSQL from the installation files, open it, create a new session with root/Password1 credentials, connect to the session, and create a database called "osTicket".
<br />

</p>
<img src="https://i.imgur.com/sT62tvd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p> Continue setting up osTicket in the browser by entering the required information, such as the help desk name, default email, MySQL database details, etc. Click "Install Now!" to complete the setup.
<br />

