<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

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
<img src="https://i.imgur.com/q04Fqns.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After creating your resource group in Microsoft Azure. Create a virtual machine, with Windows 10 and 2-4 virtual CPU's. Add a username and password to the VM and now it is time to start installing files for osTIcket.
</p>
<br />


<p>
<img src="https://i.imgur.com/nkF1tjp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
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
</p>
<p>

</p>
<br />



<p>
<img src="https://i.imgur.com/M8SsTcL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this section, I will be installing "PHP Manager for IIS", "Rewrite Module", "PHP 7.3.8", MySQL", osTIcket then finally create a "C:/PHP" directory. After installing all files, open IIS as an admin, register PHP from withing IIS, reload IIS (open IIS, stop and start the server).
  
Go to sites -> Default -> osTicket, on the right, click “Browse *:80”, go back to IIS, sites -> Default -> osTicket, double-click PHP Manager, click “enable or disable an extension”, enable: php_imap.dll, Enable: php_intl.dll, enable: php_opcache.dll, refresh the osTicket site in your browse, observe the changes, Rename: ost-config.php, from: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php, to: C:\inetpub\wwwroot\osTicket\include\ost-config.php

</p>
<br />
