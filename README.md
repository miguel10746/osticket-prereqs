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
Now, we create a new directory in the C: drive. This done by creating a new folder by right clicking on the the C: drive and naming the folder PHP.
</p>

![image](https://github.com/user-attachments/assets/8a027675-f147-437e-b7f9-f08a7026cad1)
<p>
Now from the os-Ticket-Installation-Files folder unzip PHP 7.3.8 into the new C:\PHP folder we just created.
</p>

![image](https://github.com/user-attachments/assets/c19e0269-2a9a-4c34-b4d9-b7f40f29fbf5)
</p>
From the installation folder we will install Microsoft Visual C++ or VC_redist.x86 to the VM.
<p>

![image](https://github.com/user-attachments/assets/4a48f639-6dde-48b8-a080-693663cce979)
<p>
Once everything has been install, install mysql 5.5 and set standard configuration and set username and password to one you will not forgot. 
</p>

![image](https://github.com/user-attachments/assets/458bd944-1d0e-4ae8-9bcc-da407a4bdb50)
![image](https://github.com/user-attachments/assets/9a4f010b-ebea-441f-91bb-9f4b613eb75d)
![image](https://github.com/user-attachments/assets/7cb46e0a-1f48-4e0b-b505-7b8c263cfa5c)
<p>
We must register PHP from within IIS, in order to do so open IIS as admin. Once it open click PHP manager and click a register new PHP version. Now we will go into the new folder or directory we created and select php-cgi.exe. Once done, stop and start the server again.
</p>

![image](https://github.com/user-attachments/assets/8763c804-3f37-459a-9ba7-8505f04ebc12)
![image](https://github.com/user-attachments/assets/5fd2003d-42d4-48fa-b90d-90af9c22b07a)
![image](https://github.com/user-attachments/assets/86a87e8f-db3f-4d8e-b275-3636d56122e5)
![image](https://github.com/user-attachments/assets/b095e070-6561-4351-b55b-65aba15652fb)

<p>
Now to install osTicket we will unzip osTicket-v1.15.8.zip and copy it to the upload folder into C:\inetpub\wwwroot. Once this is done we rename the folder to osTicket. 
</p>

![image](https://github.com/user-attachments/assets/cfc99bae-b82a-4899-9894-c0a78a619241)
<p>
We will go back into IIS and stop and start the server again to update the changes.
</p>

![image](https://github.com/user-attachments/assets/0a04f043-8998-446a-9d39-a238b0a24f3d)
![image](https://github.com/user-attachments/assets/5f7b9443-1f73-4448-9f21-fc7234d23008)

<p>
Once everything is done within IIS. Go to sites then Default Web Sites finally osTicket. On the right column click the link Browse *:80.
</p>

