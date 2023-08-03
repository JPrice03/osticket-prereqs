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

- Create an Azure VM(Virtual Machine) Windows 10, 4vCPUs
- Install/Enable IIS in Windows with CGI and Common HTTP Features
 World Wide Web Services -> Application Development Features ->
[X] CGI
[X] Common HTTP Features
AND IIS Management Console
Internet Information Services -> Web Management Tools -> IIS Management Console
	[X] IIS Management Console
- from the google drive folder https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
- from the google drive folder https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6, download and install the Rewrite Module (rewrite_amd64_en-US.msi)
- Create the directory C:\PHP
- from the google drive folder https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP
- from the google drive folder https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6, download and install VC_redist.x86.exe.
- from the google drive folder https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
- Typical Setup ->Launch Configuration Wizard (after install) ->Standard Configuration ->Password1(for example)
- Open IIS as an Admin
- Register PHP from within IIS
- Reload IIS (Open IIS, Stop and Start the server)
- Install osTicket v1.15.8
- download osTicket from google drive folder https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
- extract and copy "upload"folder to c:\inetpub\wwwroot
- Within c:\inetpub\wwwroot, Rename"upload" to "osTicket"
- Reload IIS (Open IIS, Stop and Start the server)
- Go to sites -> Default -> osTicket
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



<h2>Installation Steps</h2>


<p>

![image](https://github.com/JPrice03/osticket-prereqs/assets/140192548/2f7c3cae-858b-44a1-9264-dee4c2762e3f)

</p>
<p>
Install/Enable IIS in Windows with CGI and Common HTTP Features
 World Wide Web Services -> Application Development Features ->
[X] CGI
[X] Common HTTP Features
AND IIS Management Console.
</p>
<br />

![image](https://github.com/JPrice03/osticket-prereqs/assets/140192548/3d3aa441-9baf-4971-8ca0-0039babd98d7)


<p>

</p>
<p>
- from the google drive folder https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
- from the google drive folder https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6, download and install the Rewrite Module (rewrite_amd64_en-US.msi)
- from the google drive folder https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP
- from the google drive folder https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6, download and install VC_redist.x86.exe.
- from the google drive folder https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi).
</p>
<br />

![image](https://github.com/JPrice03/osticket-prereqs/assets/140192548/6be9f9db-5b64-4ed5-ae36-60b3fd9b825b)

<p>

</p>
<p>
Typical Setup ->Launch Configuration Wizard (after install) ->Standard Configuration ->Password1(for example).
</p>
<br />

![image](https://github.com/JPrice03/osticket-prereqs/assets/140192548/1ba20f3b-d7be-40bc-a9b8-49ad14f6cf07)

Open IIS as an Admin
- Register PHP from within IIS
- Reload IIS (Open IIS, Stop and Start the server)
- Install osTicket v1.15.8
- download osTicket from google drive folder https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
- extract and copy "upload"folder to c:\inetpub\wwwroot
- Within c:\inetpub\wwwroot, Rename"upload" to "osTicket"
- Reload IIS (Open IIS, Stop and Start the server)
- Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
