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
- install MySQL 5.5.62

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/gtPlBvy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I started by creating a virtual machine and running it on the Azure portal platform. After I downloaded the osTicket-Installation-Files.zip within the Virtual Machine and unzipped it onto the desktop. The folder's name was “osTicket-Installation-Files” and so after I extracted the zipped files, later on, I would use the files in this folder to install osTicket and some of the dependencies.
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
Right after I created a new folder C:\PHP, so i could unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder. Next From the “osTicket-Installation-Files” folder, I install VC_redist.x86.exe. Moreover from within the same folder I installed MySQL 5.5.62 (mysql-5.5.62-win32.msi).



</p>
<br />

<p>
<img src="https://i.imgur.com/19V3v5n.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Moreover, I opened IIS as an Admin and then, registered PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe), after I reloaded IIS which I had just opened IIS, stopped and started the server. Then after I Installed osTicket v1.15., From the “osTicket-Installation-Files” folder, unzipped “osTicket-v1.15.8.zip” and copied the “upload” folder into “c:\inetpub\wwwroot” Within “c:\inetpub\wwwroot”, which I renamed from “upload” to “osTicket”. Then once again I stopped and started the server. Finally, I went to sites -> Default -> osTicket on the right, clicked “Browse *:80” and the osTicket installer site opened up.


</p>
<br />
