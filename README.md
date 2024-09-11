# osticket-prereqs


<p>
Create an Azure Virtual Machine Windows 10, 4 vCPUs
Name: osticket-vm
Username: labuser
Password: osTicketPassword1!
  
  <p><img width="1225" alt="Screenshot 2024-09-11 at 1 03 39 PM" src="https://github.com/user-attachments/assets/0854d48a-2733-4807-8f0d-2dd862a370b1">
<img width="1225" alt="Screenshot 2024-09-11 at 1 04 01 PM" src="https://github.com/user-attachments/assets/96092e5b-55da-4203-8440-0c83347373d0">
<img width="1225" alt="Screenshot 2024-09-11 at 1 04 20 PM" src="https://github.com/user-attachments/assets/aaf1e708-d5d0-4fcb-ae59-8cd32b4b4e49">
<img width="1225" alt="Screenshot 2024-09-11 at 1 05 09 PM" src="https://github.com/user-attachments/assets/ed808a1a-b1a5-4924-bfec-7e99be3b7c4d">











Log into the VM with Remote Desktop
<img width="1225" alt="Screenshot 2024-09-11 at 1 05 37 PM" src="https://github.com/user-attachments/assets/982dc190-629a-4dfd-817e-f512272b993e">

Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”
We will use the files in this folder to install osTicket and some of the dependencies.
<img width="1225" alt="Screenshot 2024-09-11 at 1 06 44 PM" src="https://github.com/user-attachments/assets/9d09cf09-3572-4b00-bea9-1472768f2a85">
<img width="1225" alt="Screenshot 2024-09-11 at 1 07 10 PM" src="https://github.com/user-attachments/assets/562ea143-b6e1-4ef2-93a2-7e4160e06072">












Install / Enable IIS in Windows WITH CGI
World Wide Web Services -> Application Development Features -> [X] CGI
<img width="1225" alt="Screenshot 2024-09-11 at 1 07 47 PM" src="https://github.com/user-attachments/assets/cf7885e9-0209-4662-b36d-6c2986ddfcdd">
<img width="1225" alt="Screenshot 2024-09-11 at 1 08 02 PM" src="https://github.com/user-attachments/assets/8598f6fc-29e6-44c6-b965-af135dc303c0">
<img width="1225" alt="Screenshot 2024-09-11 at 1 08 18 PM" src="https://github.com/user-attachments/assets/5ec0d082-5ad5-4332-9102-7afa31dcb2f0">

<img width="1225" alt="Screenshot 2024-09-11 at 1 09 52 PM" src="https://github.com/user-attachments/assets/b2e6327d-19bf-4da9-95c1-8c43444359ee">
<img width="1225" alt="Screenshot 2024-09-11 at 1 10 36 PM" src="https://github.com/user-attachments/assets/9b48425d-3df0-4119-9d1d-f4bce27cfcc3">



From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)
<img width="1225" alt="Screenshot 2024-09-11 at 1 11 22 PM" src="https://github.com/user-attachments/assets/5965ba35-9d79-4714-8ab3-6e89f258af56">



Create the directory C:\PHP
<img width="1225" alt="Screenshot 2024-09-11 at 1 12 39 PM" src="https://github.com/user-attachments/assets/9d2449cf-73c0-4264-bd6f-59a9b4acaa66">
<img width="1225" alt="Screenshot 2024-09-11 at 1 12 58 PM" src="https://github.com/user-attachments/assets/cab5f91e-3c4f-41dc-bf16-560a3411fbb1">



From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
<img width="1225" alt="Screenshot 2024-09-11 at 1 14 04 PM" src="https://github.com/user-attachments/assets/9e1ce224-6d28-4999-9a18-4ebe83202855">





from the “osTicket-Installation-Files” folder, install VC_redist.x86.exe
<img width="1225" alt="Screenshot 2024-09-11 at 1 15 20 PM" src="https://github.com/user-attachments/assets/60405e2d-56ba-4272-8698-4f33856eeb87">



From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
Username: root
Password: root
<img width="1225" alt="Screenshot 2024-09-11 at 1 16 03 PM" src="https://github.com/user-attachments/assets/b4acf403-2b33-4fd6-9063-8927c2e9d6a3">
<img width="1225" alt="Screenshot 2024-09-11 at 1 16 39 PM" src="https://github.com/user-attachments/assets/3f7f3016-80da-489f-a321-3458400345e4">
<img width="1225" alt="Screenshot 2024-09-11 at 1 17 01 PM" src="https://github.com/user-attachments/assets/eecf5613-a656-475b-a209-378b0cffd141">



Open IIS as an Admin(Right click)
<img width="1225" alt="Screenshot 2024-09-11 at 1 19 05 PM" src="https://github.com/user-attachments/assets/3a101597-b906-4024-a5ca-0604105179c6">


Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
<img width="1225" alt="Screenshot 2024-09-11 at 1 19 55 PM" src="https://github.com/user-attachments/assets/6c0473e8-28e2-4718-915a-ad55f4e8a174">
<img width="1225" alt="Screenshot 2024-09-11 at 1 20 22 PM" src="https://github.com/user-attachments/assets/3531ede3-f80b-4fa9-a3dc-4fc2a64ca387">
<img width="1225" alt="Screenshot 2024-09-11 at 1 21 17 PM" src="https://github.com/user-attachments/assets/4df7ab0b-69ae-4150-902d-702647f4fd7e">
<img width="1225" alt="Screenshot 2024-09-11 at 1 21 27 PM" src="https://github.com/user-attachments/assets/a182f6f7-e0ac-4b6c-a180-88d56bc2327e">


Reload IIS (Open IIS, Stop and Start the server)
<img width="1225" alt="Screenshot 2024-09-11 at 1 21 49 PM" src="https://github.com/user-attachments/assets/05d768cc-ad2e-48e9-993b-2c1648ca100f">


Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
<img width="1225" alt="Screenshot 2024-09-11 at 1 23 10 PM" src="https://github.com/user-attachments/assets/6f7eeca5-2ae6-4192-8cf4-539a9c9c9c67">
<img width="1225" alt="Screenshot 2024-09-11 at 1 26 31 PM" src="https://github.com/user-attachments/assets/86226cf3-fbc3-471b-aba1-f4df67a35083">
<img width="1225" alt="Screenshot 2024-09-11 at 1 26 51 PM" src="https://github.com/user-attachments/assets/227e1f67-45be-4fc2-b35f-353f516752e3">

Reload IIS (Open IIS, Stop and Start the server)
<img width="1225" alt="Screenshot 2024-09-11 at 1 27 04 PM" src="https://github.com/user-attachments/assets/12ab840c-a739-46f2-b63e-843737fcb069">


Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
<img width="1225" alt="Screenshot 2024-09-11 at 1 27 53 PM" src="https://github.com/user-attachments/assets/189dcb7c-783b-4250-b5e4-02de85a045f3">



Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes
<img width="1225" alt="Screenshot 2024-09-11 at 1 28 02 PM" src="https://github.com/user-attachments/assets/1a982599-13e1-4d34-ab88-1b0cd387b2fc">
<img width="1225" alt="Screenshot 2024-09-11 at 1 28 54 PM" src="https://github.com/user-attachments/assets/28a484f1-c606-4c1c-bf5a-cf1d43835ec5">
<img width="1225" alt="Screenshot 2024-09-11 at 1 29 20 PM" src="https://github.com/user-attachments/assets/c66252e6-562a-4db1-a21d-ca4a5e0f785d">
<img width="1225" alt="Screenshot 2024-09-11 at 1 29 20 PM" src="https://github.com/user-attachments/assets/db71fe30-86ff-4ac2-ad59-d8e4ef26917a">


Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
<img width="1225" alt="Screenshot 2024-09-11 at 1 30 31 PM" src="https://github.com/user-attachments/assets/02a34615-3ed2-497a-afb0-69dac8149110">
<img width="1225" alt="Screenshot 2024-09-11 at 1 30 44 PM" src="https://github.com/user-attachments/assets/9bdc5077-ba2a-45ea-9a90-bcfbc708ff4c">
<img width="1225" alt="Screenshot 2024-09-11 at 1 31 04 PM" src="https://github.com/user-attachments/assets/ffbaf0c4-5085-4c99-9010-e741e95ae922">

Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All
<img width="1225" alt="Screenshot 2024-09-11 at 1 31 04 PM" src="https://github.com/user-attachments/assets/01a70741-8f0f-414c-8861-062b3392d43c">
<img width="1225" alt="Screenshot 2024-09-11 at 1 31 17 PM" src="https://github.com/user-attachments/assets/baaf532a-c86f-44ed-966a-bfd5d18420bb">
<img width="1225" alt="Screenshot 2024-09-11 at 1 31 42 PM" src="https://github.com/user-attachments/assets/909d457a-bb2f-44ef-b64a-f0e42a7154a8">
<img width="1225" alt="Screenshot 2024-09-11 at 1 32 06 PM" src="https://github.com/user-attachments/assets/c2905fed-a6e3-4e15-b4c0-bcf8affeef25">


Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)
<img width="1225" alt="Screenshot 2024-09-11 at 1 32 34 PM" src="https://github.com/user-attachments/assets/105992ff-f7d0-4e9b-9637-880ef49e533a">
<img width="1225" alt="Screenshot 2024-09-11 at 1 33 12 PM" src="https://github.com/user-attachments/assets/251eb144-9e0f-4b3b-965a-c60b3df39f2b">



From the “osTicket-Installation-Files” folder, install HeidiSQL.
Open Heidi SQL
Create a new session, root/root
Connect to the session
Create a database called “osTicket”
<img width="1225" alt="Screenshot 2024-09-11 at 1 33 50 PM" src="https://github.com/user-attachments/assets/69c8b661-dc67-4281-825c-ab15d7a4f739">
<img width="1225" alt="Screenshot 2024-09-11 at 1 34 03 PM" src="https://github.com/user-attachments/assets/2b605833-4f01-4b6f-bed1-fd504618bf7e">
<img width="1225" alt="Screenshot 2024-09-11 at 1 34 25 PM" src="https://github.com/user-attachments/assets/cf98e2c3-d1d9-4de5-aad3-df2761dd87dc">
<img width="1225" alt="Screenshot 2024-09-11 at 1 34 58 PM" src="https://github.com/user-attachments/assets/2a1e2feb-691a-403b-ada5-370d2262ad11">
<img width="1225" alt="Screenshot 2024-09-11 at 1 35 30 PM" src="https://github.com/user-attachments/assets/09367f41-113a-4320-9915-4a3450d73231">

Continue Setting up osTicket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click “Install Now!”
<img width="1225" alt="Screenshot 2024-09-11 at 1 36 36 PM" src="https://github.com/user-attachments/assets/ff559b16-c9b5-46d8-9421-6c8ca40e7b43">


Browse to your help desk login page: http://localhost/osTicket/scp/login.php
this is for admin/ person who does the ticket
<img width="1225" alt="Screenshot 2024-09-11 at 1 37 54 PM" src="https://github.com/user-attachments/assets/9fa4e9ca-b817-4c67-bd07-3b15bf90fae3">
<img width="1225" alt="Screenshot 2024-09-11 at 1 38 20 PM" src="https://github.com/user-attachments/assets/04922cff-1c9c-4743-bb2c-4a3ebc317215">

End Users osTicket URL:
http://localhost/osTicket/ 
this if for end user submitting ticket
<img width="1225" alt="Screenshot 2024-09-11 at 1 38 37 PM" src="https://github.com/user-attachments/assets/5880b1fd-7796-456f-b875-a636f2ca681c">




