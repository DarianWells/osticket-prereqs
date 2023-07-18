<p align="center">
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

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p> 
  
1. Install and enable IIS.

2. On the windows search bar, type control panel and click on the control panel application

3. Go to "programs"

4. Select "Turn Windows Features On or Off"

5. Find folder Internet Information Servives. Check the box and then expand the folder.

6. Enable CGI services. Go to Internet Information Services > World Wide Web Services > Application Developement Features > CGI. 

7. Enable Common HTTP Features. Go to Internet Information Services > World Wide Web Services > Common HTTP Features. Check the boxes on all features under this folder.

8. Select "OK".

9. Windows will install/enable IIS. Once that finishes, select close. You can also close out the control panel window.

10. Open up a new tab in any web browser. In the address bar, type in "127.0.0.1". It should display a Windows Information Services webpage. This confirms that IIS was successfully installed. If that page doesn't display, try uninstalling and then reinstalling IIS. You can do this by going back to the control panel > programs > Turn windows features on or off > Internet Information Services. Uncheck this box and select ok. Then re-check the box and select ok. Try connecting to the webpage again.

11. Download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) https://www.iis.net/downloads/community/2018/05/php-manager-150-for-iis-10

12. Download and install URL Rewrite Module (rewrite_amd64_en-US.msi) https://www.iis.net/downloads/microsoft/url-rewrite

13. Open the file explorer. In the search bar, type "C:" and press enter. On the C: drive, create a folder named "PHP".

14. Download PHP 8.2.8 (the non thread safe zip file) https://windows.php.net/download/ . Extract all Contents into the PHP folder that was created on the C: drive.

15. Install Microsoft Visual Redistributable VC_redist.x86.exe https://www.microsoft.com/en-us/download/details.aspx?id=48145
  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p> 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
