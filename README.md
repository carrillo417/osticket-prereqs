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

- Windows 10 Pro </b> (22H2)

<h2>List of Prerequisites</h2>

- Create a Resourse Group in Azure
- Create an Azure Virtual Machine Windows 10, 2 vCPUs
- Have <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">Installation Files</a> available


<h2>Installation Steps</h2>
                        
- Connect to Virtual Machine using Remote Desktop
- Within the VM, download the osTicket-Installation-Files.zip and unzip onto the desktop

  <img src="https://i.imgur.com/u5kGR2P.png" height="80%" width="80%" alt=""/>

  <img src="https://i.imgur.com/LSuBNUA.png" height="80%" width="80%" alt=""/>

- Install/Enable IIS in Windows with CGI
  - Open Control Panel
  - Under Programs click on Uninstall program
  - Click on Turn Windows Features on or off

  <img src="https://i.imgur.com/vTRiEam.png" height="80%" width="80%" alt=""/>

  - Select Internet Information Services
  - Click the + button on World Wide Web Services
  - Expand Application Development Features
  - Enable CGI and Click OK

<img src="https://i.imgur.com/I9TjLXf.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/yNyeEQ0.png" height="80%" width="80%" alt=""/>

- Install PHP Manager for IIS from the "osTicket-Installation-Files" folder
- Install the Rewrite Module as well

<img src="https://https://i.imgur.com/wnYekaU.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/defkgu8.pngg" height="80%" width="80%" alt=""/>

- Create the directory C:\PHP

<img src="https://i.imgur.com/d7XjdN2.png" height="80%" width="80%" alt=""/>

- From the "osTicket-Installation-Files" folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

<img src="https://i.imgur.com/El1RFQE.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/6QV606L.png" height="80%" width="80%" alt=""/>

- From the "osTicket-Installation-Files" folder, install VC_redist.x86.exe
- Install MySQL 5.5.62

<img src="https://i.imgur.com/Kvxt1Bo.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/VyzLPz6.png" height="80%" width="80%" alt=""/>

- Follow the following steps for setting up correctly:
- Typical setup -> Launch Configuration Wizard after install -> Standard Configuration
- Username: root
- Password: root
- (Using this username and password for an easier install and setup, not recommended in real scenarios)

<img src="https://i.imgur.com/uq77c57.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/0avZ9dZ.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/GZ5BY5n.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/TzO4idD.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/XnlYM7Q.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/BPsKxaE.png" height="80%" width="80%" alt=""/>

- Open IIS as an Admin
- Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
  
<img src="https://i.imgur.com/XNwhOha.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/X7NZ1BX.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/41ftOZp.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/8vAMX2P.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/u3EuCwI.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/cphKsMg.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/dmg5bgP.png" height="80%" width="80%" alt=""/>

- Reload IIS (Stop and Start the server) 

<img src="https://i.imgur.com/7k9sfiy.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/UKAsTZZ.png" height="80%" width="80%" alt=""/>

- Install osTicket v1.15.8
- From the "osTicket-Installation-Files" folder, unzip "osTicket-v1.15.8.zip"

<img src="https://i.imgur.com/5Y20ZHW.png" height="80%" width="80%" alt=""/>

- Copy the "upload" folder into "c:\inetpub\wwwroot"

<img src="https://i.imgur.com/2qpnIS1.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/6SAk4RJ.png" height="80%" width="80%" alt=""/>

- Within "c:\inetpub\wwwroot", Rename "upload" to "osTicket" (Make sure it is spelled exactly as shown, otherwise it will not work)

<img src="https://i.imgur.com/HrcjdZD.png" height="80%" width="80%" alt=""/>

 - Reload IIS
 - Go to sites -> Default -> osTicket
 - on the right, click "Browse *.80"

<img src="https://i.imgur.com/1mXXNQd.png" height="80%" width="80%" alt=""/>

- Note that some extensions are not enabled
- Go back to IIS, sites -> Default -> osTicket
- Double clikc PHP Manager
- Click "Enable or disable an extension"
- Enable: php_imap.dll
- Enable: php_intl.dll
- Enable: php_opcache.dll
- Refresh the osTicket site on your browser and observe the changes

<img src="https://i.imgur.com/85cHsrA.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/X4ALhwO.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/8KHd1Of.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/QenR1TV.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/QGeFdIn.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/QGeFdIn.png" height="80%" width="80%" alt=""/>

- Rename os-config.php
- from: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to: C:\inetpub\wwwroot\osTicket\include\ost-config.php

<img src="https://i.imgur.com/xozjii9.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/r0HJAxv.png" height="80%" width="80%" alt=""/>

- Assign permissions: ost-config.php
- Disable inheritance -> Remove All
- New Permission -> Everyone -> All (Again, this isn't ideal for real life scenarios)

<img src="https://i.imgur.com/d3ZysoL.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/Eh13hyS.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/b8Odcn9.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/7SS3Jof.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/uVD4Dbn.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/WTzh2lP.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/v0BYbFX.png" height="80%" width="80%" alt=""/>

- Continue Setting up osTicket in the browser (Click Continue)
- Name Helpdesk
- Default Email

<img src="https://i.imgur.com/sL7eOCl.png" height="80%" width="80%" alt=""/>

- From the “osTicket-Installation-Files” folder, install HeidiSQL

<img src="https://i.imgur.com/R1381k0.png" height="80%" width="80%" alt=""/>

- Open HeidiSQL
- Create a new session, username: root password: root
- Connect to the session

<img src="https://i.imgur.com/FF3Vffn.png" height="80%" width="80%" alt=""/>

- Create a Database called "osTicket"

<img src="https://i.imgur.com/DYEg6wV.png" height="80%" width="80%" alt=""/>

<img src="https://i.imgur.com/lcUHbBc.png" height="80%" width="80%" alt=""/>

- Continue setting up osTicket in the browser
- MySQL Database: osTicket
- MySQL username: root
- MySQL password: root
- Click "Install Now!"

<img src="https://i.imgur.com/roGiL09.png" height="80%" width="80%" alt=""/>

-Congratulations! osTicket should be installed with no errors.

<img src="https://i.imgur.com/KsQRjZA.png" height="80%" width="80%" alt=""/>
