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

- IIS
- PHP manager
- Rewrite Module
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>
<<img width="623" height="345" alt="image" src="https://github.com/user-attachments/assets/412922bf-c50b-47ac-a791-a3502b5688ba" />
"/>
</p>
<p>

  First, I logged into Microsoft Azure and created a virtual machine with Windows 10 and 4 vCPUs.
</p>
<br />

<p>
<img width="816" height="414" alt="image" src="https://github.com/user-attachments/assets/9a0cfbbe-9738-4f6b-b86e-11701444cbcf" />
<"/>
</p>
<p>
Then I connected to the virtual machine using Remote Desktop by entering the public IP address assigned to the virtual machine.
</p>
<br />

<p>
<<img width="1143" height="303" alt="image" src="https://github.com/user-attachments/assets/0aac8a8c-50a3-40e3-bbd9-079b7ef84859" />

</p>
<p>
From within the virtual machine I dowloaded the osTicket instalation file https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD
</p>  and unzipped it to my desktop by clicking the tab labeled "compressed folder tools" and clicking "extract all" after the folder is unzipped I drag and drop the folder onto the desktop. 
<br />


<img width="1119" height="501" alt="image" src="https://github.com/user-attachments/assets/2a0685d1-c743-411a-8aab-592763839857" />

Next I enabled IIS with CGI by going to the control panel and clicking programs then clicking "turn windows features on or off" I then clicking on the drop down beside "Internet Information Services" then "World Wide web Services" and "Application Development Features"  and checked the box next to CGI.



<img width="998" height="446" alt="image" src="https://github.com/user-attachments/assets/18b18772-9e40-4f77-ba0b-3c343dd80c76" />

From within the osTicket installations file folder I installed the PHP manager and rewrite module by double clicking them and following the prompts.


<img width="1594" height="745" alt="image" src="https://github.com/user-attachments/assets/1c2936c1-f6b5-448c-b38f-938ab70eb2fe" />

Next I went to file explorer under "this PC" and "Windows" then created a new folder named "PHP" and then extraced the php file to the new PHP folder. Then I installed the VC_redist and mysql files by double clicking them and following the prompt. For mysql I did the typical setup and launched Configuration Wizard after install, then I selected the standard configuration and for the username and password used "root".


<img width="1186" height="616" alt="image" src="https://github.com/user-attachments/assets/ffe1d78c-ce90-4ac1-9db3-9359ed19bfb2" />


Then I used the search bar at the bottom of the screen to search "Internet Information System (IIS) Manager" and right clicked it then selected open as administrator.


<img width="1489" height="788" alt="image" src="https://github.com/user-attachments/assets/d28a53ed-fea2-49d0-8225-e382a8fcdf60" />


From here I clicked on the PHP manager and then clicked "Register new PHP". I clicked the three dots and selected this option under This PC-Windows-PHP


<img width="1479" height="766" alt="image" src="https://github.com/user-attachments/assets/16c59208-64cf-44db-83cb-2c827b73526f" />

Now that I have registered the new PHP I am going to restar it by clicking osTicket on the right side of the window under "Connections" then clicking the "stop" and "start" functions on the left side of the window under "Manage Server"


<img width="1748" height="735" alt="image" src="https://github.com/user-attachments/assets/002427e1-7624-4b56-917f-2294cc1ce8fa" />

From within the "osTicket-Installation-Files" folder I unzipped "osTicket-v1.15.8.zip" and copied the upload file to "c:\inetpub\wwwroot" using the drag and drop method. Then I renamed the "upload" folder to "osTicket" an restarted IIS again.


img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.

img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.


