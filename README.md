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
<img src="https://i.imgur.com/gh1IFQw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/IiToWy2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In azure, we join client-1 to the domain controller by setting the DNS of client-1 to the private IP address of the domain controller (in this case, 10.0.0.6). After restarting the virtual machine in Azure, we log into client one. We go to settings and then the about tab. We go to "rename this pc" and change the domain. We enter the domain that the server is apart of and we get the confirmation that we have successfully joined the server.
</p>
                                                                                                 <p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the client machine has been joined to the domain, we go back into the domain controller. From here, we enable remote desktop for all users. Normally this should be implemented along with a policy, but for the purposes of this example we will keep it simple. We will then run powershell ISE as an adminstrator and use a pre-written script to populate active directory with random users
</p>
                                                                                                 
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the client machine has been joined to the domain, we go back into the domain controller. From here, we we enable remote desktop for all users. Normally this should be implemented along with a policy, but for the purposes of this example we will keep it simple.
</p>                                                                                                
<br />
