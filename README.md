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




  
