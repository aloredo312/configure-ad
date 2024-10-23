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
<img width="650" alt="organizational_unit" src="https://github.com/user-attachments/assets/14da59d7-30e4-404d-8ae9-8e721476f4ae">
<img width="645" alt="new_user" src="https://github.com/user-attachments/assets/d511c139-1c26-4b4d-aa3b-c6d2bb6121a0">
<img width="585" alt="user_to_admin" src="https://github.com/user-attachments/assets/9ddd02f3-9ef8-42ce-9662-7a6429e52194">
</p>
<p>
To create a Domain Admin user within the domain we need to go to Adminsitrative Tools and go into Active Directory Users and Computers. We will right click mydomainname.com go under New and click on Organizational Unit type in a name (_EMPLOYEES) and click ok. We can repeat the process to create more Organizational Units for example another could be _Admins. We can create a new employee by rigth clicking on one of the Organizational Units like _Admins and going to New and select User. A window will pop up that will ask to fill in their full name and userlogin name, click next and it will ask to create a paswword. If we want to make the user a proper admin we have to go to their name right click and click on properties. We will have to click on the Member of tab, click Add we can then search for the Domain Admins name. Once found click on Ok and then Apply and now they are an Admin User.
</p>
<br />

<p>
<img width="878" alt="computer:domain_name_change" src="https://github.com/user-attachments/assets/2aac82c6-e36b-4bcf-99c6-11605cd56239">
<img width="417" alt="account_with_permission" src="https://github.com/user-attachments/assets/46adb5a7-8d7f-4bb7-bb18-524b1c1f0180">
</p>
<p>
To get Client-1 to join our domain (mydomain.com) we need to be in Client-1's VM and go into the system settings and go into the About. On the right side click on Rename this PC (advanced). System properties will open and under the Computer Name tab click on Change. Under member of check the circle Domain and type the domain name for example "mydomain.com" and click ok. It will ask for an account that has permission to join the domain, here we can use the admin user we created earlier "mydomain.com\jane_admin if successful it will do a restart.
</p>
<br />
