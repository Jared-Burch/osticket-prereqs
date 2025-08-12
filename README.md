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

- Web Server
- Operating System
- PHP
- MySQL database
- osTicket package

<h2>Installation Steps</h2>

<p>
<<img width="623" height="345" alt="image" src="https://github.com/user-attachments/assets/412922bf-c50b-47ac-a791-a3502b5688ba" /><p>

  First, I logged into Microsoft Azure and created a virtual machine with Windows 10 and 4 vCPUs.


<img width="816" height="414" alt="image" src="https://github.com/user-attachments/assets/9a0cfbbe-9738-4f6b-b86e-11701444cbcf" />

Then I connected to the virtual machine using Remote Desktop by entering the public IP address assigned to the virtual machine.


<<img width="1143" height="303" alt="image" src="https://github.com/user-attachments/assets/0aac8a8c-50a3-40e3-bbd9-079b7ef84859" />

From within the virtual machine I dowloaded the osTicket instalation file and unzipped it to my desktop by clicking the tab labeled "compressed folder tools" and clicking "extract all" after the folder is unzipped I drag and drop the folder onto the desktop. 



<img width="1119" height="501" alt="image" src="https://github.com/user-attachments/assets/2a0685d1-c743-411a-8aab-592763839857" />

Next I enabled IIS with CGI by going to the control panel and clicking programs then clicking "turn windows features on or off" I then clicking on the drop down beside "Internet Information Services" then "World Wide web Services" and "Application Development Features"  and checked the box next to CGI.



<img width="998" height="446" alt="image" src="https://github.com/user-attachments/assets/18b18772-9e40-4f77-ba0b-3c343dd80c76" />

From within the osTicket installations file folder I installed the PHP manager and rewrite module by double clicking them and following the prompts.



<img width="1594" height="745" alt="image" src="https://github.com/user-attachments/assets/1c2936c1-f6b5-448c-b38f-938ab70eb2fe" />

Next I went to file explorer under "this PC" and "Windows" then created a new folder named "PHP" and then extracted the PHP file to the new PHP folder. Then I installed the VC_redist and mysql files by double clicking them and following the prompt. For mysql I did the typical setup and launched Configuration Wizard after install, then I selected the standard configuration and for the username and password used "root".



<img width="1186" height="616" alt="image" src="https://github.com/user-attachments/assets/ffe1d78c-ce90-4ac1-9db3-9359ed19bfb2" />

Then I used the search bar at the bottom of the screen to search "Internet Information System (IIS) Manager" and right clicked it then selected open as administrator.



<img width="1489" height="788" alt="image" src="https://github.com/user-attachments/assets/d28a53ed-fea2-49d0-8225-e382a8fcdf60" />

From here I clicked on the PHP manager and then clicked "Register new PHP". I clicked the three dots and selected this option under This PC-Windows-PHP



<img width="1479" height="766" alt="image" src="https://github.com/user-attachments/assets/16c59208-64cf-44db-83cb-2c827b73526f" />

Now that I have registered the new PHP I am going to restart it by clicking osTicket on the right side of the window under "Connections" then clicking the "stop" and "start" functions on the left side of the window under "Manage Server"



<img width="1748" height="735" alt="image" src="https://github.com/user-attachments/assets/002427e1-7624-4b56-917f-2294cc1ce8fa" />

From within the "osTicket-Installation-Files" folder I unzipped "osTicket-v1.15.8.zip" and copied the upload file to "c:\inetpub\wwwroot" using the drag and drop method. Then I renamed the "upload" folder to "osTicket" an restarted IIS again.



<img width="1064" height="559" alt="image" src="https://github.com/user-attachments/assets/36ee61f3-1a6c-4a5b-83a8-26219673239e" />

Next under PHP manager I clicked "enable or disable an extension" and then enabled  php_imap.dll,  php_intl.dll, and  php_opcache.dll by right clicking each one and clicking "enable".



<img width="872" height="692" alt="image" src="https://github.com/user-attachments/assets/5cf00ca0-d943-4378-9032-69bf05741aaa" />

I opened file explorer and renamed :"C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php" to "C:\inetpub\wwwroot\osTicket\include\ost-config.php"



<img width="872" height="716" alt="image" src="https://github.com/user-attachments/assets/6792a69b-4bc3-41ee-b8e7-a3d7cd7e2b2c" />

Then I right clicked the file and clicked properties, then the security tab and clicked "Advanced". From here I clicked "Disable inheritance" to remove all inherited permissions. 



<img width="757" height="562" alt="image" src="https://github.com/user-attachments/assets/a4401121-14e2-4a33-b66f-6ac6ab37f07e" />

Now I click "Add" then "select a principal" and type "Everyone" in the text box and give everyone full control.



<img width="1074" height="726" alt="image" src="https://github.com/user-attachments/assets/6fb6a683-54f5-4049-8a3f-26e5da1944a8" />

From the osTicket installer homepage I clicked continue and filled out the prompt using "adminuser" as the username for the admin account and "Password1!" as the password.



<img width="911" height="345" alt="image" src="https://github.com/user-attachments/assets/e8b5a64c-c1ef-448c-b295-eaa79c3ad8ef" />

Before moving on with the prompt I went to the "osTicket-Installation-Files" folder and installed HeidiSQL by double clicking the file and following the prompt.



<img width="685" height="481" alt="image" src="https://github.com/user-attachments/assets/022951c6-b039-47d4-8e6e-32f11ce5159a" />

From here I clicked "New" and used the password "root" then clicked "open"



<img width="929" height="592" alt="image" src="https://github.com/user-attachments/assets/b15a5a92-f236-4c66-b6e8-a9f9a4dfb4e8" />

Next I created a new database by right clicking "Unnamed" from the dropdown on the left side of the screen and clicked "create database" and named it "osTicket"



<img width="562" height="369" alt="image" src="https://github.com/user-attachments/assets/ca3907eb-0f55-4b9a-9a36-dbde5aa1c380" />

Now I completed the form on the osTicket installer webpage and used the MySQL database as "osTicket" to perfectly match the database name we created in the last step. I use "root" as the username and password as well.

At this point I have successfully installed osTicket and am ready to use the software!
