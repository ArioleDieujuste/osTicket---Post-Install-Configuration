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

</p>
<br />
