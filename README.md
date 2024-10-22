<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Deployment and Configuration Steps</h2>

<p>
<img width="1247" alt="install_active_directory" src="https://github.com/user-attachments/assets/dbf8fc34-0e76-4362-a1d3-24f1a4db1312">
<img width="890" alt="domain_name" src="https://github.com/user-attachments/assets/f9d5144c-cc3e-4270-9a27-63d96668d781">
<img width="390" alt="new_login" src="https://github.com/user-attachments/assets/93140bd1-8274-41be-87a8-b7bad9e39fe1">
</p>
<p>
To install Active Directory Services we need to log into DC-1, go to Server Manager, go to Add roles and features. Once the first window comes up we will keep clicking next until we get to a section where we need to check the box for Active Directory Domain Services and we will say add features, then just finish setting up until we can install it. Then in the Server Manager we will see a flag in the top right corner, click it and window with a link that says Promote this server to a domain controller will pop up. Once clicked a new window will pop up, check the box that says Add a new forest and type a domain name in the box, click next create a password and then click next until you are able to install. It will restart on its own, and for us to log back in we will have to use the domain name we used and the user for example: mydomain.com\labuser.
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
