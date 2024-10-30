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
