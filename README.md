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

- Step 1: Deployment of Domain Controller and Client Desktop in Azure
- Step 2: Remote Into Server, Download Active Directory, and Promote Server to Domain Controller
- Step 3
- Step 4

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/rzkuGYt.png"80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, we create the domain controller and the client desktop we will be using in this lab. We start by creating a resource group within Azure, and then from there we create two virtual machines. We must ensure that both virtual machines are located within the same region and are on the same network. One will be configured as a server, the other will be configured as a desktop running on the windows 10 operating system.
</p>
<br />

<p>
<img src="https://i.imgur.com/tnWwa6y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p><img src="https://i.imgur.com/wIX19Jd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After the virtual machines have been created, we remote into the server. From the server manager, we download active directory domain services. Once that has been downloaded, we click the flag in the top right and turn the server into a domain controller. The active directory tab should be there once the computer restarts.
</p>
<br />

<p>
<img src="https://i.imgur.com/5taHASY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From there, we create an organization for admins and an organization for users. We then create an admin account named Jane Doe and we use it to log into the client-1 virtual machine.
</p>
                                                                                                 <p>
<img src="https://i.imgur.com/BXQtukV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In azure, we join client-1 to the domain controller by setting the DNS of client-1 to the private IP address of the domain controller (in this case, 10.0.0.6).
</p>
                                                                                                 <p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
