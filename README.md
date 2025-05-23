<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Starting Requirements and Installation</h1>
This lesson delineates the starting requirements and installation steps of the osTicket help desk platform.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure's Virtual Machine Platform
- Microsoft Windows App
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Starting Requirement Steps</h2>

- Enable Internet Information Services (IIS)
- Install Required osTicket Applications and Components
- Install osTicket and Configure Permissions

<h2>Installation Steps</h2>

<p><img width="1127" alt="Screenshot 2025-03-27 at 7 12 20 PM" src="https://github.com/user-attachments/assets/c767acd1-bae4-4017-949e-612b5394394f" />
<p>
Upon creating the Windows 10 virtual machine (VM) in Microsoft Azure and logging into it through the Windows App, I began the process of downloading the osTicket installation zip files on the desktop. I went to the Search bar and entered "Control Panel" > clicked on "Uninstall Programs" > clicked on "Turn Windows features on or off." I then scrolled down to Internet Information Services (IIS) > clicked on it > and then I clicked "OK." The files then downloaded to the Virtual Machine (VM). I also installed the "CGI" folder onto the VM, thereby providing the means to search for the 127.0.0.1 address on Virtual Machine's web browser.
<br />
<p><img width="831" alt="Screenshot 2025-03-28 at 12 59 46 PM" src="https://github.com/user-attachments/assets/97bb8e16-f108-40fe-a425-c610eefc9de5" />
<p>
Following the initial download of the osTicket installation files, I began downloading each major application and component needed for successful deployment of osTicket (PHP Manager, Rewrite Module, C++ Redistributable, mySQL, etc.). I proceeded forward by establishing the mySQL server with the typical set-up and standard security configuration through Configuartion Wizard. I then created a root username and password. Next, I opened Internet Information Services (IIS) Manager in Administrator mode and registered the PHP through PHP Manager. Lastly,I reloaded the IIS by first returning to IIS Manager Administrator start window, stopping the server by clicking the "Stop" option, and then starting the server again by clicking the "Start" option.
</p>
<br />
<p>
<img width="1120" alt="Screenshot 2025-03-28 at 3 31 09 PM" src="https://github.com/user-attachments/assets/6bc961de-2b37-44fd-b8b2-5f32dbafe6bd" />
<p>
With most of the osTicket installation files downloaded, I started the installation of osTicket v.1.15.8 from its zip file and uploaded the automated "upload" folder into the "wwwroot" folder ("Windows C:" > "inetpub" > "wwwroot"). I then renamed the "upload" file to "osTicket." I once again stopped and started the Internet Information Services (IIS) through IIS Manager in Administrator mode. 
</p><img width="1680" alt="Screenshot 2025-03-28 at 4 12 25 PM" src="https://github.com/user-attachments/assets/c56e9003-4142-483e-b665-7282fcc7e9a0" />
<p>
  
Still in Administator mode of IIS Manager, I opened the "Sites" folder > "Default Web Site" folder > and then clicked "osTicket" folder. I subsequently double-clicked the browse folder "Browse *:80 (http)," which launched the webpage to the "osTicket Installer." From there, I enabled the three necessary remaining extensions for osTicket (php_imap.dll, php_intl.dll, php_opcache.dll) through PHP Manager and then refreshed the "osTicket Installer" browser page. I then renamed the "ost-sampleconfig.php" folder to "ost-config.php ("Windows C:" > "inetpub" > "wwwroot" > "osticket" > "include" > "ost-sampleconfig.php"). I also right-clicked to rename the folder and right-clicked to "Properties" to assign permissions to select users. Having established the necessary extensions and configurations thus far, I created my osTicket administrator account with the helpdesk name, email, and recently installed "HeidiSQL" with a database named "osTicket."
</p>
<br />

