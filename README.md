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

- Install / Enable IIS
- PHP Manager for IIS V1.5.0
- Rewrite Module 
- PHP 7.3.8
- VC_redist.x86.exe
- MySQL 5.5.62
- osTicket v1.15.8
- Heidi SQL 12.3.0.6589

<h2>Installation Steps</h2>

<p> 

**This list is pretty long, so please follow every step in order*

**Install and enable IIS.**

1. On the windows search bar, type control panel and click on the control panel application

2. Go to "programs"

3. Select "Turn Windows Features On or Off"

4. Find folder Internet Information Servives. Check the box and then expand the folder.

5. Enable CGI services. Go to Internet Information Services > World Wide Web Services > Application Developement Features > CGI. 

6. Enable Common HTTP Features. Go to Internet Information Services > World Wide Web Services > Common HTTP Features. Check the boxes on all features under this folder.

7. Select "OK".

8. Windows will install/enable IIS. Once that finishes, select close. You can also close out the control panel window.

9. Open up a new tab in any web browser. In the address bar, type in "127.0.0.1". It should display a Windows Information Services webpage. This confirms that IIS was successfully installed. If that page doesn't display, try uninstalling and then reinstalling IIS. You can do this by going back to the control panel > programs > Turn windows features on or off > Internet Information Services. Uncheck this box and select ok. Then re-check the box and select ok. Try connecting to the webpage again.

The rest of the programs needed are sourced from this Installation File List: https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

**PHP Manager for IIS**

1. From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

**Rewrite Module**

1. From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi)

**PHP 7.3.8**

1. Open the file explorer. In the search bar, type "C:" and press enter. On the C: drive, create a folder named "PHP".

2. From the Installation Files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip). Extract all Contents into the PHP folder that was created on the C: drive.

**VC Redist**

1. From the Installation Files, download and install VC_redist.x86.exe.

**MySQL 5.5.62**

1. From the Installation Files, Download and install MySQL 5.5.62.
      - Typical Setup
      - Launch Configuration Wizard (after setup)
      - Standard Configuration
      - Enter in Password1 for the password
      - Click "execute"


1. Now search IIS in the windows search bar and right click and select "run as administrator"

19. Click on "PHP Manager"

20. Select Register new PHP version

21. Browse files to C:/PHP and select the php-cgi file that is located within that folder.

22. Now the PHP manager should display the version of PHP installed

23. In IIS, click on the home icon in the top right corner. Reload the servers by clicking "stop" and then "start"

**osTicket v1.15.8**

1. Next, download osTicket from the installation files folder

26. Extract the zip file and copy the "upload" folder to c:\inetpub\wwwroot

27. Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

28. Reload IIS again by stopping and restarting the server.

29. In IIS, on the left side, browse to sites -> default -> osTicket

30. On the right side, click browse .80

31. It should display a webpage with the osTicket installer.

32. If you notice on the osTicket webpage, not all extensions are enable. Now we will make changes in order to enable all extensions for osTicket.

33. Go back to IIS, sites -> Default -> osTicket

34. Double-click PHP Manager

35. Click “Enable or disable an extension”
      - Enable: php_imap.dll
      - Enable: php_intl.dll
      - Enable: php_opcache.dll

36. Refresh the osTicket site in your browse, observe the changes

37. Browse to C:-> inetpub-> wwwroot -> osTicket -> include -> "ost-sampleconfig.php"

38. Rename "ost-sampleconfig.php" to "ost-config.php"

39. Right click on that same file and select "Properties"
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

**Heidi SQL**

1. Install HeidiSQL from the Installation Files list.

41. In HeidiSQL create a new connection to the database. We will use the same user and password that was used when installing MySQL.
      - Click "new"
      - User: root
      - Password: Password1
      - Select "Open"

42. Create an osTicket database in HeidiSQL
      - Right click on 'Unnamed' on the upper left side and select "Create new" -> "Database"
      - Name the Database "osTicket". Select "OK"

43. Finish installation for osTicket
      - Return to the osTicket installation webpage
      - MySQL Database: osTicket
      - User: root
      - Password: Password1
      - Click "Install Now"

44. osTicket has been successfully installed!

For final cleanup,

1. delete the "setup" folder located at C:\inetpub\wwwroot\osTicket\setup

2. Reset the permissions for ost-config.php to read-only
      - go to C:\inetpub\wwwroot\osTicket\include\ost-config.php
      - Right click the ost-config.php
      - Properties -> Security tab -> Advanced
      - Edit the permissions for "Everyone"
      - Uncheck every box except for "Read" and "Read & execute"

46. Now the has been fully completed. There are two different URLs used to access the osTicket ticketing system. One for Admins and Support personnel, another for customers who want to submit tickets.
    - Admins: http://localhost/osTicket/scp/login.php
    - End User (customer login): http://localhost/osTicket/ 
  
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
