<h1>Setting up the lab</h1>


<h2>Description</h2>
The first stage of this home lab involved deploying a Windows Server 2022 virtual machine and configuring it as a Domain Controller using Active Directory Domain Services (AD DS). The goal was to build a foundation for a small enterprise-style network where users, computers, authentication and security policies can be managed centrally.

The lab was built using VMware Workstation, with an isolated host-only network to provide a safe environment for testing Windows Server administration without affecting my main network.

<h2>Environment</h2>

Virtualisation: VMware Workstation

Operating System: Windows Server 2022 Standard

Server hostname: JH-DC01

Domain name: jakehomelab.test

Server IP address: 192.168.193.10/24

Server role: Domain Controller

Roles installed: Active Directory Domain Services (AD DS) and DNS Server

<h2>Implementation</h2>

1. Virtual Machine and Network Configuration

Created a Windows Server 2022 virtual machine and configured a static IPv4 address to ensure the server remained accessible at a consistent address. The server was connected to an isolated host-only virtual network.
<img src="Screenshots/Power on VM.png"/>
2. Active Directory Domain Services

Installed the AD DS role through Server Manager and promoted the server to a Domain Controller. Created a new Active Directory forest using the domain name jakehomelab.test.
<img src="Screenshots/Roles and sever.png"/>

3. DNS Configuration and Verification

Configured DNS as part of the Domain Controller setup. Created and verified the relevant DNS records, including forward and reverse lookup records, to support hostname resolution across the lab environment.

Used PowerShell, nslookup and dcdiag /test:dns to investigate DNS behaviour and verify that the domain controller and its DNS configuration were functioning correctly.

<h2>Outcome</h2>

Successfully established the initial Active Directory environment, providing a foundation for the next stages of the project. This environment will be expanded with domain users, organisational units (OUs), security groups, Group Policy and a Windows client machine to simulate common IT support scenarios.

<h2>Skills Demonstrated</h2>

Windows Server installation and configuration

Virtual machine and network setup

Active Directory Domain Services deployment

Domain Controller promotion and forest creation

DNS configuration and troubleshooting

PowerShell and command-line diagnostics
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Diskpart</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>
<p align="center">
Launch the utility: <br/>
<img src="Screenshots/Power on VM.png"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
