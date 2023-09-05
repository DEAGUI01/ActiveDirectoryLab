<h1>Active Directory Home Lab</h1>


<h2>Description</h2>
In this project I create an Active Directory Home lab environment using Oracle Virtual Box. Esentially, I emulate a mini corporate network. Configuring and running this lab certainly helped develop my understanding of how active directory and windows networking works as well as my skills with Powershell. 
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Oracle Virtual Box</b>
- <b>Windows Active Directory</b>
- <b>Windows Server 2019</b>
<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
- <b>Windows Server 2019</b> 

<h2>Network Diagram </h2>
<img src="https://i.imgur.com/s0gLaFr.png" height="80%" width="80%" alt="Network Diagram"/>
<br />
<br />

<h2>Project walk-through:</h2>

<p align="center">

Create Virtual Machine (this will be the Domain Controller) and install Windows Server on it <br/>
<img src="https://i.imgur.com/8c9ucUA.png" height="80%" width="80%" alt="Windows Server VM"/>
<br />
<br />
Create password for built-in admin account  <br/>
<img src="https://i.imgur.com/ZFUwrGB.png" height="80%" width="80%" alt="built-in admin pw"/>
<br />
<br />
Rename Internal and External (Internet) networks <br/>
<img src="https://i.imgur.com/A0UaY40.png" height="80%" width="80%" alt="rename networks"/>
<br />
<br />
Configure Internal Network with a static IP and make the DNS server the same IP since this will be the domain controller  <br/>
<img src="https://i.imgur.com/QMFmbwS.png" height="80%" width="80%" alt="configure internal network"/>
<br />
<br />
Install Active Directory Domain Services on the Server <br/>
<img src="https://i.imgur.com/C0bcGNQ.png" height="80%" width="80%" alt="install AD DS"/>
<br />
<br />
Configure Active Directory Domain Services, create the domain <br/>
<img src="https://i.imgur.com/CT2l5JD.png" height="80%" width="80%" alt="create domain"/>
<br />
<br />
Create Admins organizational unit in Active Directory and administrator user <br/>
<img src="https://i.imgur.com/ImLMrdy.png" height="80%" width="80%" alt="admin account creation"/>
<br />
<br />
Install Remote Access on the Server <br/>
<img src="https://i.imgur.com/5iZJ3li.png" height="80%" width="80%" alt="install remote access"/>
<br />
<br />
Configure and enable Routing and Remote Access <br/>
<img src="https://i.imgur.com/x60Ml86.png" height="80%" width="80%" alt="configure remote access"/>
<br />
<br />
Install DHCP on the server <br/>
<img src="https://i.imgur.com/QoVuU8j.png" height="80%" width="80%" alt="install DHCP"/>
<br />
<br />
Configure DHCP and create New Scope for IPV4 <br/>
<img src="https://i.imgur.com/oHhO9By.png" height="80%" width="80%" alt="configure DHCP"/>
<br />
<br />
Add users to Active Directory using Powershell script <br/>
<img src="https://i.imgur.com/T2qvSzb.png" height="80%" width="80%" alt="add users"/>
<br />
<br />
Create a client Virtual Machine and install Windows 10 on it <br/>
<img src="https://i.imgur.com/FpnhMWv.png" height="80%" width="80%" alt="create client machine"/>
<br />
<br />
Check that the client's network configuration is correct and ping an internet address to confirm internet access <br/>
<img src="https://i.imgur.com/u4gsPcC.png" height="80%" width="80%" alt="check client's ipconfig"/>
<br />
<br />
Change the machine name to reflect it is a client and join the domain <br/>
<img src="https://i.imgur.com/8Ke6R05.png" height="80%" width="80%" alt="change client's name and join domain"/>
<br />
<br />
On the Domain Controller, using DHCP check that a lease was created for the new client <br/>
<img src="https://i.imgur.com/hpuRxhf.png" height="80%" width="80%" alt="check client's lease"/>
<br />
<br />
On the Domain Controller, using Active Directory, check that the client computer was added to the domain <br/>
<img src="https://i.imgur.com/nCctz9L.png" height="80%" width="80%" alt="check client joined the domain"/>
<br />
<br />
Log into the client computer as any of the users that were created with the Powershell script to confirm that the whole environment works as intended<br/>
<img src="https://i.imgur.com/7QnApgm.png" height="80%" width="80%" alt="final check"/>

</p>


