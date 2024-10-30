<h1>Active Home Directory Lab</h1>


<h2>Description</h2>
Today, I’ll show you how I set up an Active Directory lab using Oracle VirtualBox! This project dives into creating a Windows networking environment from scratch, covering essentials like Active Directory, PowerShell, and Windows Server. This hands-on lab builds a strong foundation in virtualization and Windows networking skills.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Oracle VirtualBox</b>
- <b>Active Directory</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
- <b>Windows Server 2019</b>

<h2>Program walk-through:</h2>

<p align="center">
To begin, here is the diagram that was used to reference and support the configuration of the AD Home lab!: <br/>
<img src="https://imgur.com/AcBdQAf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Intsalling Windows Server 2019 on VirtualBox:  <br/>
<img src="https://imgur.com/E3oxrpv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/DS8ydRd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Setting up the IP adressing for the internal NIC: <br/>
<img src="https://imgur.com/6zcCz5H.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p align="center">
We know Ethernet 2 was the internal adapter because it was assigned an APIPA address due to not finding a DHCP server.
<p align="center">
I renamed both adapters to make it easy.: </b>

<img src="https://imgur.com/Lo18NZm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configuring the IP addressing for the internal network:  <br/>
<img src="https://imgur.com/8x4u7HX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Installing Active Directory Domain Services from server manager:  <br/>
<img src="https://imgur.com/UQwclOc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Deployment and Creating the Domain:  <br/>
<img src="https://imgur.com/5D9ZfWp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Creating an admin OU and adding a user:  <br/>
<img src="https://imgur.com/oyVivxj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Making the account a domain admin:  <br/>
<img src="https://imgur.com/DbWU7C3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Logging into the new admin account:  <br/>
<img src="https://imgur.com/NOvzcXz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Installing ras/nat to allow users to connect to internal server AND connect to internet:  <br/>
<img src="https://imgur.com/S0rhdJX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/0kYVk0Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configuring it with the routing and remote access tool:  <br/>
<img src="https://imgur.com/DbWU7C3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/BvUVim3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/8z7oEuT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/EzcUVnQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Adding a DHCP server so users can get a IP address and access the internet while being on the internal private server:  <br/>
<img src="https://imgur.com/LxYPxiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Creating the Scope:  <br/>
<img src="https://imgur.com/jkiK2Sb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Setting the range:  <br/>
<img src="https://imgur.com/SZ2MYmu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Success:  <br/>
<img src="https://imgur.com/KbmtBmg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Executing a Powershell Script to add 1000+ Users (Thanks Josh Madakor):  <br/>
<img src="https://imgur.com/29zCHeW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Adding and running the script in PowerShell:  <br/>
<img src="https://imgur.com/HlNaosd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
All the new users added:  <br/>
<img src="https://imgur.com/43uQjlh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Adding the windows 10 client, changing the adapter to the internal network.:  <br/>
<img src="https://imgur.com/8JaYR9t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Pinging google and the domain to make sure it works.:  <br/>
<img src="https://imgur.com/6sdQxg7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Changing the computer name and joining the domain using credentials from one of the users.:  <br/>
<img src="https://imgur.com/rR2bdMU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirming if the new computer has shown up on the domain controller.:  <br/>
<img src="https://imgur.com/9iOm6uQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Signing in as the "abargo" user:  <br/>
<img src="https://imgur.com/dNhRbTg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirming we are logged into the domain on CLIENT1 as user abargo.:  <br/>
<img src="https://imgur.com/haHnqUz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Summary:  <br/>
<img src="https://imgur.com/8W9fujk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
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
