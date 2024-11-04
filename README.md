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

- Download osTicket installation files.
- install PHP Manager for IIS 
-  install the Rewrite Module and unzip PHP 7.3.8
- install VC_redist.x86.exe and install MySQL 5.5.62
- Install osTicket v1.15.8 and HeidiSQL.

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/gtPlBvy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I started by creating and running a virtual machine on the Azure portal platform. After I downloaded the osTicket-Installation-Files.zip within the Virtual Machine and unzipped it onto the desktop. The folder's name was “osTicket-Installation-Files” and so after I extracted the zipped files, later on, I would use the files in this folder to install osTicket and some of the dependencies.
</p>
<br />

<p>
<img src="https://i.imgur.com/5bEmk67.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I opened up the control panel then made my way through programs and programs and features, then I clicked on Turn Windows features on or off, then made my way to
World Wide Web Services -> Application Development Features -> and finally I checked marked CGI to enable it. Next, I installed PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) from which I grabbed from the From the “osTicket-Installation-Files” folder. Moreover, from within the same folder I installed the Rewrite Module (rewrite_amd64_en-US.msi).

</p>
<br />

<p>
<img src="https://i.imgur.com/8CfNJxQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Right after I created a new folder C:\PHP, so I could unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder. Next From the “osTicket-Installation-Files” folder, I install VC_redist.x86.exe. Moreover from within the same folder I installed MySQL 5.5.62 (mysql-5.5.62-win32.msi).



</p>
<br />

<p>
<img src="https://i.imgur.com/19V3v5n.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Moreover, I opened IIS as an Admin and then, registered PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe), after I reloaded IIS which I had just opened IIS, stopped and started the server. Then after I Installed osTicket v1.15., From the “osTicket-Installation-Files” folder, unzipped “osTicket-v1.15.8.zip” and copied the “upload” folder into “c:\inetpub\wwwroot” Within “c:\inetpub\wwwroot”, which I renamed from “upload” to “osTicket”. Then once again I stopped and started the server. Finally, I went to sites -> Default -> osTicket on the right, clicked “Browse *:80” and the osTicket installer site opened up.


</p>
<br />

<p>
<img src="https://i.imgur.com/Me4y8dR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Some extensions were not enabled as you can see in the previous image so I went back to IIS, sites -> Default -> osTicket Double-clicked PHP Manager then Clicked “Enabled or disable an extension” and then enabled, php_imap.dll, php_intl.dll, php_opcache.dll, then so after I Refreshed the osTicket site, and observed the changes as you can see in the current image. Moreover, I renamed a PHP File ost-sampleconfig.php to ost-config.php,
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Next, I Assigned Permissions: ost-config.php, then 
Disabled inheritance -> Removed All
New Permissions -> Everyone -> All.

</p>
<br />

<p>
<img src="https://i.imgur.com/fKuCiq3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In my last step, I Continued Setting up osTicket in the browser by filling in the information the empty boxes were asking for, such as,
Name: Helpdesk and
Default email: (receives email from customers)

From the “osTicket-Installation-Files” folder, I installed HeidiSQL. then I
Opened Heidi SQL,
Created a new session, root/root were the username and password.
Connected to the session then,
Created a database called “osTicket”

Lastly, I continued setting up osTicket in the browser and fill in the descriptions such as,
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root then
clicked on “Install Now!”


</p>
<br />
