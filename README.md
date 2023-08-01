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

16. 16. Download and install MySQL 5.5.62. You can find an archived version linked here: https://downloads.mysql.com/archives/community/
    -Typical Setup
    - Launch Configuration Wizard (after setup)
    - Standard Configuration
    - Enter in Password1 for the password
    - Click "execute"
17. Now search IIS in the windows search bar and right click and select "run as administrator"

18. Click on "PHP Manager"

19. Select Register new PHP version

20. Browse files to C:/PHP and select the php-cgi file that is located within that folder.

21. Now the PHP manager should display the version of PHP installed

22. In IIS, clcick on the home icon in the top right corner. Reload the servers by clicking "stop" and then "start"

23. Next, download osTicket from the installation files folder.

24. Extract the zip file and copy the "upload" folder to c:\inetpub\wwwroot

25. Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

26. Reload IIS again by stopping and restarting the server.

27. In IIS, on the left side, browse to sites -> default -> osTicket

28. On the right side, click browse .80

29. It should display a webpage with the osTicket installer.

30. If you notice on the osTicket webpage, not all extensions are enable. Now we will make changes in order to enable all extensions for osTicket.

31. Go back to IIS, sites -> Default -> osTicket

32. Double-click PHP Manager

33. Click “Enable or disable an extension”
    - Enable: php_imap.dll
    - Enable: php_intl.dll
    - Enable: php_opcache.dll

34. Refresh the osTicket site in your browse, observe the changes

35. Browse to C:-> inetpub-> wwwroot -> osTicket -> include -> "ost-sampleconfig.php"

36. Rename "ost-sampleconfig.php" to "ost-config.php"

37. Right click on that same file and select "Properties"
   - Go to the "Security" tab
   - Click "Advanced"
   - Click "Disable inheritance"
   - Select "Remove all inherited permissions from this object."
   - Click "Add"
   - Click "Select a principal"

38. Type "everyone" in the text box then click "Check Names"
   - Select "OK"
   - Enable "Full Control" and select "OK", the window will close.
   - Select "Apply" then select "OK" to close the Advanced Security window.
   - Select "OK" to close the ost-config.php Properties window.

39. Go back to the osTicket browser page
    - Click "Continue"
    - Helpdesk Name is (Your Name) Help Desk
    - Defaul email (receives email from customers)
    - Fill out the rest of the information to create the admin user account. Make sure you remember the username and password
    - Before continuing, Heidi SQL must be installed in order to fill out the Database Settings information

40. Install HeidiSQL from the Installation Files list.

41. In HeidiSQL create a new connection to the database. We will use the same user and password that was used when installing MySQL.
    - Click "new"
    - User: root
    - Password: Password1
    - Select "Open"

42. Create an osTicket database in HeidiSQL
    - Right click on 'Unnamed' on the upper left side and select "Create new" -> "Database"
    - Name the Database "osTicket". Select "OK"

43. Finish installation for osTicket
    - Returun to the osTicket installation webpage
    - MySQL Database: osTicket
    - User: root
    - Password: Password1
    - Click "Install Now"
  
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
