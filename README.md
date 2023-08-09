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
<img width="960" alt="1, right click start select run" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/2d4fcf29-29eb-40b7-9772-19cea9a4420d">


2. Go to "programs"

3. Select "Turn Windows Features On or Off"
<img width="960" alt="2, windows features on or off" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/56f97828-64e3-4382-8106-5308f283fde7">

4. Find folder Internet Information Servives. Check the box and then expand the folder.
<img width="960" alt="3, Internet information services" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/de4c2277-86b8-4c08-bf74-ea6869d7e32f">


5. Enable CGI services. Go to Internet Information Services > World Wide Web Services > Application Developement Features > CGI. 
<img width="960" alt="4, Enable CGI" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/6f2e2e34-16c9-4a85-8474-ddf3e6d848ec">

6. Enable Common HTTP Features. Go to Internet Information Services > World Wide Web Services > Common HTTP Features. Check the boxes on all features under this folder.
<img width="960" alt="6, Enable HTTP features checked" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/a02ac00e-20c0-4a95-a81a-6505436b815b">

7. Select "OK".

8. Windows will install/enable IIS. Once that finishes, select close. You can also close out the control panel window.
<img width="960" alt="9, IIS Installation Complete" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/40146814-f590-465d-b3ac-531f3389bbde">

9. Open up a new tab in any web browser. In the address bar, type in "127.0.0.1". It should display a Windows Information Services webpage. This confirms that IIS was successfully installed. If that page doesn't display, try uninstalling and then reinstalling IIS. You can do this by going back to the control panel > programs > Turn windows features on or off > Internet Information Services. Uncheck this box and select ok. Then re-check the box and select ok. Try connecting to the webpage again.
<img width="960" alt="10, web browser check for IIS install ok" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/10733445-4564-4c1f-8b47-5d0c6f39a2ac">

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
<img width="960" alt="18 Open IIS run as admin" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/9d71506d-cd82-42f5-bc32-4760f811bee1">

19. Click on "PHP Manager"
<img width="960" alt="19 select PHP Manager" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/c86b933e-f52a-4360-ad4e-f5554a8f5a66">

20. Select Register new PHP version
<img width="960" alt="20 register new PHP version" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/5c3be27d-ea61-44d0-b29e-f9d84ad35ce0">

21. Browse files to C:/PHP and select the php-cgi file that is located within that folder.
<img width="465" alt="21 (redo) browse to PHP and select PHP CGI" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/e8ab9370-a3c7-467c-9be0-42684f8f6e60">

22. Now the PHP manager should display the version of PHP installed

23. In IIS, click on the home icon in the top right corner. Reload the servers by clicking "stop" and then "start"

**osTicket v1.15.8**

1. Next, download osTicket from the installation files folder

26. Extract the zip file and copy the "upload" folder to c:\inetpub\wwwroot
<img width="938" alt="23 copy upload folder to c-inetpub-wwwroot" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/0f44b548-38b4-47a0-9370-9a8188bb220c">

27. Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
<img width="616" alt="24 rename upload to osticket" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/8d5e69c4-7149-405d-9515-ead8282da733">

28. Reload IIS again by stopping and restarting the server.

29. In IIS, on the left side, browse to sites -> default -> osTicket

30. On the right side, click browse .80
<img width="960" alt="25 browsee iis - sites - default - osticket then click browse" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/6f10b8df-8e65-427b-b07b-24a52d964457">

31. It should display a webpage with the osTicket installer.
<img width="960" alt="26 OS ticket successfully installed" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/c4f06b35-a07c-4a09-b8ad-fc8a50186988">

32. If you notice on the osTicket webpage, not all extensions are enable. Now we will make changes in order to enable all extensions for osTicket.

33. Go back to IIS, sites -> Default -> osTicket

34. Double-click PHP Manager

35. Click “Enable or disable an extension”
      - Enable: php_imap.dll
      - Enable: php_intl.dll
      - Enable: php_opcache.dll
<img width="960" alt="27 php manager enable extensions" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/55645471-5908-4462-9ac2-1be1e445cafb">
<img width="960" alt="28 enable extensions" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/b5554053-0690-4cd3-8649-bec09602eb50">

36. Refresh the osTicket site in your browse, observe the changes
<img width="960" alt="29 osticket extension changes" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/8608010d-a58a-4447-8478-3e5c1a53d3b2">

37. Browse to C:-> inetpub-> wwwroot -> osTicket -> include -> "ost-sampleconfig.php"

38. Rename "ost-sampleconfig.php" to "ost-config.php"
<img width="616" alt="31 rename ost config change" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/b31bcf28-e204-49f3-bbeb-cb7840c1459b">

39. Right click on that same file and select "Properties"
     - Go to the "Security" tab
     - Click "Advanced"
     - Click "Disable inheritance"
     - Select "Remove all inherited permissions from this object."
     - Click "Add"
     - Click "Select a principal"
<img width="960" alt="32 ost-config, properties, security, advanced, disable inheritance" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/661ca7ac-2f2e-45d0-be2d-14e2623cfa1b">
<img width="685" alt="33 select a principal, everyone" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/c6170472-faf2-47be-9ba1-a8ed1d9782ef">


38. Type "everyone" in the text box then click "Check Names"
     - Select "OK"
     - Enable "Full Control" and select "OK", the window will close.
     - Select "Apply" then select "OK" to close the Advanced Security window.
     - Select "OK" to close the ost-config.php Properties window.
<img width="683" alt="34 full control" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/741232aa-e4df-41ae-a4d9-8113c87ba967">

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
<img width="513" alt="36 Heidi SQL new connection" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/ab0b07f7-8016-42fe-9c81-901dc12294b4">
<img width="514" alt="37 heidisql user and password click open" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/a08522fb-6b37-422e-af3b-48b5387be7cf">

42. Create an osTicket database in HeidiSQL
      - Right click on 'Unnamed' on the upper left side and select "Create new" -> "Database"
      - Name the Database "osTicket". Select "OK"
<img width="698" alt="38 HeidiSQL create osticket database" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/b526137e-f898-4a02-8851-99735ac2b82a">

43. Finish installation for osTicket
      - Return to the osTicket installation webpage
      - MySQL Database: osTicket
      - User: root
      - Password: Password1
      - Click "Install Now"
<img width="960" alt="39 finish osticket install" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/bdbe9afd-f9d4-48a6-a3fe-8a0d571e71b3">
<img width="960" alt="39 finish osticket install" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/05fc8bdf-e6c3-4776-b142-18fc5a81a009">

44. osTicket has been successfully installed!
<img width="960" alt="40 final osTicket Installed successfully" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/4fa6685c-1b13-404a-a1bc-96a98a90a482">

For final cleanup,

1. delete the "setup" folder located at C:\inetpub\wwwroot\osTicket\setup
<img width="610" alt="41 delete setup folder" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/4a233d18-5a59-40f0-a0d7-b9b360bc2202">

2. Reset the permissions for ost-config.php to read-only
      - go to C:\inetpub\wwwroot\osTicket\include\ost-config.php
      - Right click the ost-config.php
      - Properties -> Security tab -> Advanced
      - Edit the permissions for "Everyone"
      - Uncheck every box except for "Read" and "Read & execute"
<img width="685" alt="42 reset permissions for ost config" src="https://github.com/DarianWells/osticket-prereqs/assets/132870202/28fd1896-fb63-4997-9a56-d0300e9fbe32">

46. Now the has been fully completed. There are two different URLs used to access the osTicket ticketing system. One for Admins and Support personnel, another for customers who want to submit tickets.
    - Admins: http://localhost/osTicket/scp/login.php
    - End User (customer login): http://localhost/osTicket/ 

