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



Open IIS as an Admin
