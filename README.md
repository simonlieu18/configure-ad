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


![image](https://github.com/user-attachments/assets/a3ffed1b-f6c7-4e7a-ad04-3fd485c89127)

<p>
Install Active Directory Domain Services on the virtual machine that'll be used as a Domain Controller.
</p>
<br />

![image](https://github.com/user-attachments/assets/b039f74a-8d31-4e62-afd2-75e38fc2c692)



<p>
Click the flag on the top right of the screen and follow the install steps to promote the server to a Domain Controller.
</p>
<br />

![image](https://github.com/user-attachments/assets/0a63058d-bc87-427e-8f52-d5075159a8dc)


<p>
Open "Active Directory Users and Computers" application and create two new organizational units, "EMPLOYEES" and "ADMINS", under your domain.
</p>
<br />


![image](https://github.com/user-attachments/assets/59cd5e35-9077-499e-a53b-9d60164d178a)


<p>
Add a new user in the "ADMINS" organizational unit, then add them to the "Domain Admins" security group. Proceed to disconnect from the Data Center and login as the newly created admin user.
</p>
<br />

![image](https://github.com/user-attachments/assets/690252eb-8ba8-4aa7-ae6f-a58c672f6f0e)

<p>
On the "client" virtual machine, you will join it to the domain by clicking the Windows icon on the bottom left. Go to "System", then "Rename this PC", then the "Change" button.
</p>
<br />


![image](https://github.com/user-attachments/assets/e24847a8-3cbe-4a04-936b-ac5eff1cea82)


<p>
Back on the Data Center machine, confirm that the new client machine is linked by opening "Active Directory Users and Computers" and navigate to the domain and open up the "Computers" organizational unit. After that make a new organizational unit called "CLIENTS" and drag that client machine into the new "CLIENTS" organizational unit.
</p>
<br />

![image](https://github.com/user-attachments/assets/d6ab3433-0a20-4369-952f-0ea1e4fc6855)

<p>
Create some users in the "EMPLOYEES" organizational unit.
</p>
<br />


![image](https://github.com/user-attachments/assets/56b534a0-3db5-4e73-a731-f38a4eec8577)


<p>
As an admin on the client machine, allow domain users access to remote desktop.
</p>
<br />

![image](https://github.com/user-attachments/assets/1033c11b-0eb9-444a-ac19-86deee71e001)


<p>
To test the newly created users, remote desktop into the client machine with a new user's login information.
</p>
<br />
