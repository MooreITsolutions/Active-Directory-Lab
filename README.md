<h1>Acvtive Directory HomeLab</h1>


<h2>Description</h2>
This project consisted of me configuring a virtual machine, to run a domain controller from which I could experiment with active directory. Thouroughly going through this lab a few times gives you a grasp of how an organization would work with users and how they could provision them. Within this lab you also learn some networking, having to configure things like a DHCP server and DNS.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Oracle Virtual Box</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
- <b>Server 2019</b> 
<h2>Program walk-through:</h2>

<p align="center">
Download and open Oracle Vitrual Box: <br/>
<img src="https://i.imgur.com/WvxlwYt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install and run Server 2019:  <br/>
<img src="https://i.imgur.com/9hMswuN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Set IP address for internal NIC. No need for default gateway, the DC is going to act as one. This Server will also be the DNS server so you can use the loopback ping address of 127.0.0.1: <br/>
<img src="https://i.imgur.com/klPhIoA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Go into server manager dashboard and install Active Directory Domain Services:  <br/>
<img src="https://i.imgur.com/Ye2NUWE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Intsall RAS/NAT to allow client to be on virtual network but still be able to access the internet:  <br/>
<img src="https://i.imgur.com/9ol784E.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure DHCP and scope for future clients to gain access to the network and be assigned IP addresses:  <br/>
<img src="https://i.imgur.com/IKAeW2Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/OAtlEBS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p align="center">
Download and open Oracle Vitrual Box <br/>
<img src="https://i.imgur.com/dKpigqL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create another VM, this one to act as a client to connect to the DC we have set up:  <br/>
<img src="https://i.imgur.com/1IekxiG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Run ipconfig in the command line to confirm IP address and default gateway of client: <br/>
<img src="https://i.imgur.com/ZLbziVd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Ping 8.8.8.8 to see if the client can reach the internet(google):  <br/>
<img src="https://i.imgur.com/30Z2HGR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Ping:  <br/>
<img src="https://i.imgur.com/ZT65b7y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

