<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Deployed in the Cloud (Azure)</h1>
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

- Install Active Directory
- Create a Domain Admin user within the domain
- Join Client to your domain
- Setup Remote Desktop for non-administrative users on Client-1

<h2>Deployment and Configuration Steps</h2>

![image](https://github.com/user-attachments/assets/40c76f82-16cf-460f-b2e0-af950e8f0580)

<p>
Launch 2 virtual machines, one working as a Domain Controller and DNS while the other virtual machine as a Client. Both should be in the same virtual network and resource group.
</p>
<br />

![image](https://github.com/user-attachments/assets/a3ffed1b-f6c7-4e7a-ad04-3fd485c89127)

<p>
Install Active Directory Domain Services on the virtual machine that'll be used as a Domain Controller.
</p>
<br />

![image](https://github.com/user-attachments/assets/47563961-58b0-4803-985b-dcda4441391d)

<p>
Click the flag on the top right of the screen to promote the server to a Domain Controller.
</p>
<br />

![image](https://github.com/user-attachments/assets/0a7236e7-b809-403d-aa64-d5a034a05ab7)


<p>
To create a domain admin user, first, create a new employee inside the "admins" organizational unit then add them to the "domain admins' security group.
</p>
<br />

![image](https://github.com/user-attachments/assets/690252eb-8ba8-4aa7-ae6f-a58c672f6f0e)

<p>
On the "client" virtual machine, you will join it to the domain.
</p>
<br />

![image](https://github.com/user-attachments/assets/1d1cc49f-bfd6-448f-854a-53574d20ea3f)


<p>
As an admin on the client machine, allow domain users access to remote desktop.
</p>
<br />

![image](https://github.com/user-attachments/assets/c892132b-7f19-4893-aa7b-f41d759a358c)


<p>
To test, sign into client machine with user information.
</p>
<br />
