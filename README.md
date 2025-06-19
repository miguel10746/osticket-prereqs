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

- Virtual Machine with Windows 10
- IIS enable with CGI
- PHP Manager
- Database: MySql 5.5+
- osTicket source files

<h2>Installation Steps</h2>

![image](https://github.com/user-attachments/assets/0284b50c-ac7b-4110-99f3-3e061a4459c6)

</p>
<p>
Once log into the VM, press windows + R, type control and hit enter. Once in the control panel I went to Programs and Features, clicked Programs, then clicked unstall or change program. Then inside click turn windows features on or off. I clicked on Internet Information Services to turn on.  
</p>

![image](https://github.com/user-attachments/assets/d60eec05-9d83-4bee-8d7a-187409233edf)
<p>
Click World Wide Web Services, to open Application Development Features and turn on CGI.
</p>
<br />

![image](https://github.com/user-attachments/assets/3fb06862-b7d8-42e1-a8b5-4362f51721e5)
<p>
Install PHP manager from the files of the osTicket.
</p>

![image](https://github.com/user-attachments/assets/f2881696-842d-48b5-9c1d-d1ad5fb4dad6)
<p>
Once PHP manager has been install. Install Rewrite Module.
</p>
<p>

![image](https://github.com/user-attachments/assets/35c0f8f2-0ae2-4bb6-b628-872eb3013421)
<p>
Now, I create a new directory in the C: drive. This done by creating a new folder by right clicking on the the C: drive and naming the folder PHP.
</p>

![image](https://github.com/user-attachments/assets/8a027675-f147-437e-b7f9-f08a7026cad1)
<p>
Now from the os-Ticket-Installation-Files folder unzip PHP 7.3.8 into the new C:\PHP folder I just created.
</p>

![image](https://github.com/user-attachments/assets/c19e0269-2a9a-4c34-b4d9-b7f40f29fbf5)
</p>
From the installation folder I install Microsoft Visual C++ or VC_redist.x86 to the VM.
<p>

![image](https://github.com/user-attachments/assets/4a48f639-6dde-48b8-a080-693663cce979)
<p>
Once everything has been install, I install mysql 5.5 and set standard configuration and set my username and password.
</p>

![image](https://github.com/user-attachments/assets/458bd944-1d0e-4ae8-9bcc-da407a4bdb50)
![image](https://github.com/user-attachments/assets/9a4f010b-ebea-441f-91bb-9f4b613eb75d)
![image](https://github.com/user-attachments/assets/7cb46e0a-1f48-4e0b-b505-7b8c263cfa5c)
<p>
I register PHP from within IIS, in order to do so I open IIS as admin. Once it open I clicked PHP manager and clicked a register new PHP version. Now I go into the new folder or directory I created and select php-cgi.exe. Once done, stop and start the server again.
</p>

![image](https://github.com/user-attachments/assets/8763c804-3f37-459a-9ba7-8505f04ebc12)
![image](https://github.com/user-attachments/assets/5fd2003d-42d4-48fa-b90d-90af9c22b07a)
![image](https://github.com/user-attachments/assets/86a87e8f-db3f-4d8e-b275-3636d56122e5)
![image](https://github.com/user-attachments/assets/b095e070-6561-4351-b55b-65aba15652fb)

<p>
Now to install osTicket I unzip osTicket-v1.15.8.zip and copy it to the upload folder into C:\inetpub\wwwroot. Once this is done I rename the folder to osTicket. 
</p>

![image](https://github.com/user-attachments/assets/cfc99bae-b82a-4899-9894-c0a78a619241)
<p>
I will go back into IIS and stop and start the server again to update the changes.
</p>

![image](https://github.com/user-attachments/assets/0a04f043-8998-446a-9d39-a238b0a24f3d)
![image](https://github.com/user-attachments/assets/5f7b9443-1f73-4448-9f21-fc7234d23008)

<p>
Once everything is done within IIS. Go to sites then Default Web Sites finally osTicket. On the right column click the link Browse *:80.
I need to enable certain extension that are disable.
</p>

<p>
  
![image](https://github.com/user-attachments/assets/18b2c4d4-0b96-4090-ab65-20b22e840928)
![image](https://github.com/user-attachments/assets/cd0076dd-ef16-4d0e-862c-827c38aaf53f)
![image](https://github.com/user-attachments/assets/2d495595-4986-400c-a86b-30740a18c396)
![image](https://github.com/user-attachments/assets/372f81b4-6d76-4417-af18-a699ddd2e379)
![image](https://github.com/user-attachments/assets/46b2b964-14f3-43a7-baab-b8f2054218ab)

<p>
Back inside the IIS I will go to sites to default to osTicket and double-click PHP Manager. Click enable or disable an extension. I will enable php_imap.dll, php_intl.dll, php_opcache.dll. Once this have been enable, refresh the the browser to see the changes take affect.
</p>

![image](https://github.com/user-attachments/assets/cc6eb10f-a24c-49a9-9c00-6cb63e96e375)
<p>
Now rename the ost-sampleconfig.php to ost-config.php. I go to C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php in the folder. Double right click and select rename folder, and change it to ost-config.php. Once this done I will remove all inheritance by double right clicking and going into properties. I set new permission to everyone to all.
</p>

![image](https://github.com/user-attachments/assets/f2103f0e-5edf-4dcd-84d1-5026ddcc4f63)

<p>
Now I will set up the osTicket in the browser.
</p>

![image](https://github.com/user-attachments/assets/5231682a-5662-4200-a54c-ca35d46a1828)
![image](https://github.com/user-attachments/assets/a8d79fb5-a62c-4876-af5e-98c3f6c638ab)
![image](https://github.com/user-attachments/assets/1c32a427-8e51-4962-8946-6e24c6404654)
![image](https://github.com/user-attachments/assets/a4b763d9-b809-4079-93dc-a96c9f312786)
<p>
Finally, I will install HeidiSql. Once install create a new session and connect to the session using the username and password from the mysql I did in the begin. Create a new database name osTicket.
</p>

![image](https://github.com/user-attachments/assets/d9ba0934-838d-4802-9621-d10a3c7cdd26)
<p>
Once HeidiSql is set up. Write the information in the browser for the osTicket to collect information into database. Once completely I clicked Install Now.
</p>

![image](https://github.com/user-attachments/assets/bb5b7c71-8b49-40f3-a1d5-bd3d1808c839)
<p>
Complete and now the osTicket is ready to be use.
</p>
