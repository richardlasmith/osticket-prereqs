# osticket-prereqs<p align="center">
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

- Create a Virtual Machine in Azure 
- Connect your Virtual Machine with Remote Desktop 
- Install PHP Manager 
- Rewrite Module 
- Download PHP 7.3.8
- Download and install VC_redist.x.86.exe
- Download and install MySQL 5.5.62
- Install osTicket 
- Enable Extensions 
- Config osTicket
- Download and Install HeidiSQL
- Set up osTicket user 

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/nykwEgi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a FREE Microsoft Azure account, Once your account is set up search "Resource Group" and Create a resource group with the name "RG-osTicket" 
</p>
<br />

<p>
<img src="https://i.imgur.com/SuxE71p.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a Virtual Machine, by searching VM. Use the Resource Group we created in step 1 "RG-osTicket". Name our new VM (Vitural Machine) VM-osTicket. Keep the region local to you. Mine is (US) East US. Scroll down to Image, and install in Windows 10 Pro, and change the size to " 2 Vcpus 16 GiB Memory for a faster processing speed. Create a VM Log in, Example Username: labuser, password: !!!Password1. * Remember your log in information. Now confirm licensing at the bottom of the page and create you new Virtual Machine. 
</p>
<br />

<p>
<img src="https://i.imgur.com/ghy0lXc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now that your Virtual Machine is created, we'll need to log into it. Search VM on Azure, and copy the public IP address. 
</p>
<br />

<p>
<img src="https://i.imgur.com/OroSSmX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For Mac users you can go to the app store and download "Microsoft Remote Desktop" for FREE. Once the application is installed. Add our VM-OSTICKET machine. PC Name: Will be the public IP Address. 
</p>
<br />

<p>
<img src="https://i.imgur.com/R7PUqk9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now log in, using the VM-OSTICKET username and password you created. * I hope you remembered this :) 
</p>
<br />

<p>
<img src="https://i.imgur.com/G8ZFkj1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Before installing PHP, We need to enable IIS in window with CGI ( Internet Information Services) * It is a web server that allow the VM to Serve up websites. OSTicket is web base). Right Click start, then search Control Panel, then Programs, click "Turn windows features on or off", Scroll down to IIS, Hit the +, and again + on World Wide Web Services. We will need to then click the + on Application Development Features and Mark "CGI" CGI lets us install PHP. OSTicket runs off of PHP.  
</p>
<br />

<p>
<img src="https://i.imgur.com/lG8VhnK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We are ready to download, PHP Manager. PHPManagerForIIS_V1.5.0.msi
</p>
<br />

<p>
<img src="https://i.imgur.com/Kyfark1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download, the rewrite module at Rewrite_amd64_en-us.msi
</p>
<br />

<p>
<img src="https://i.imgur.com/paojyql.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download, the rewrite module at Rewrite_amd64_en-us.msi This allows a special config for OSTicket. Create Directory in a new folder on C: Drive called PHP
</p>
<br />

<p>
<img src="https://i.imgur.com/9JqgCEk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) Once downloaded, ExactALL in the Newly created PHP folder. 
</p>
<br />

<p>
<img src="https://i.imgur.com/StGXAzn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We need to now download and install VC_redist.x86.exe. This is required by PHP
</p>
<br />

<p>
<img src="https://i.imgur.com/nvOXWYy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Let's Download and install MySQL 5.5.62 (mysql-5.5.62-win32) Go to Typical Setup, Launch Configuration Wizard (after install) Standard Configuration, Password1. Then Execute. Keep your PW, Username will be Root. * This is installing a database on the VM to storage user information. 
<br />
  
<p>
<img src="https://i.imgur.com/Kj6YNdm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Time to do some configurations on IIS. Make sure to run as Admin. Register new PHP Verison Located in the newly created PHP folder in C: Drive. * Restart IIS 
<br />
  
<p>
<img src="https://i.imgur.com/wsd0DgQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Download osTicket, unzip and drag the upload folder into "inetpub/ wwwroot 
<br />
  
<p>
<img src="https://i.imgur.com/EnRENFf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Rename the upload folder "osTicket. Next go to sites, default web site, osTicket. On the right side of IIS you will see browse *:80 (http)
<br />
  
<p>
<img src="https://i.imgur.com/EnRENFf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Re
<br />
