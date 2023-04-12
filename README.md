<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install-Configuration</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Post-Install-Configuration](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Web Server
- Microsoft Azure
- osTicket
- PHP
- MySQL

<h2>Installation Steps</h2>
<p>
<img src="https://i.imgur.com/M8SsTcL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this section, I will be installing "PHP Manager for IIS", "Rewrite Module", "PHP 7.3.8", MySQL", osTIcket then finally create a "C:/PHP" directory. After installing all files, open IIS as an admin, register PHP from withing IIS, reload IIS (open IIS, stop and start the server).
  
Go to sites -> Default -> osTicket, on the right, click “Browse *:80”, go back to IIS, sites -> Default -> osTicket, double-click PHP Manager, click “enable or disable an extension”, enable: php_imap.dll, Enable: php_intl.dll, enable: php_opcache.dll, refresh the osTicket site in your browse, observe the changes, Rename: ost-config.php, from: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php, to: C:\inetpub\wwwroot\osTicket\include\ost-config.php

  Reload IIS (Open IIS, Stop and Start the server)

Install osTicket v1.15.8
Download osTicket from the Installation Files Folder
Extract and copy “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

Reload IIS (Open IIS, Stop and Start the server)

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browse, observe the changes

Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All

Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)

From the Installation Files, download and install HeidiSQL.
Open Heidi SQL
Create a new session, root/Password1
Connect to the session
Create a database called “osTicket”

Continue Setting up osticket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: Password1
Click “Install Now!”

Congratulations, hopefully it is installed with no errors!
Browse to your help desk login page: http://localhost/osTicket/scp/login.php

End Users osTicket URL:
http://localhost/osTicket/ 

Clean up
Delete: C:\inetpub\wwwroot\osTicket\setup
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Notes:
Browse to your help desk login page: http://localhost/osTicket/scp/login.php  
End Users osTicket URL: http://localhost/osTicket/ 
  
</p>
<br />
