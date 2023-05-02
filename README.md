<p align="center">
 <img src="https://i.imgur.com/cLOWZFd.jpg" height="80%" width="80%" alt="VM logo"/>
</p>

<h1>Creating a DHCP relay</h1>


<h2>Description</h2>

Welcome to another setup demonstration! Today, we'll be showcasing how to set up a DHCP relay - a powerful tool that simplifies network management and eliminates the need for multiple DHCP servers. Imagine you have a DHCP server in one part of your network, but your devices are scattered across different networks. Without a DHCP relay, those devices won't be able to obtain an IP address from the server. However, with a DHCP relay, you can easily forward the requests from devices on different networks to the server, and relay the server's response back to the devices. This not only streamlines the IP address assignment process, but also helps centralize the management of your network. So if you're looking for an effective way to optimize your network management, a DHCP relay is definitely worth considering.
<br />

<h2>Environments Used </h2>

 <b>Windows Server 2019 </b> <p>
 <b>Hyper-V</b></p>

<h2>Program walk-through:</h2>

<p align="center">


<br />
From Server Manager, select Tools > Routing and Remote Access.
Expand IPv4.
 <br/>
<img src="https://i.imgur.com/S2CseAY.png" height="80%" width="80%" alt="DHCP"/>
<br />
<br />
Expand IPv4. Right-click General and select New Routing Protocol.
 <br/>
<img src="https://i.imgur.com/sMHK1Or.png" height="80%" width="80%" alt="DHCP"/>
<br />
<br />
Select DHCP Relay Agent and then select OK.

 <br/>
<img src="https://i.imgur.com/KVEBXfg.png" height="80%" width="80%" alt="DHCP"/>
<br />
<br />
From the left pane, right-click DHCP Relay Agent and select New Interface.
Select NetTeam and then select OK.

<br/>
<img src="https://i.imgur.com/JlEw6TU.png" height="80%" width="80%" alt="DHCP"/>
<br />
<br />
Make sure Relay DHCP packets is selected.
Set the boot threshold to 0 (zero).
Select OK.

 <br/>
<img src="https://i.imgur.com/lPYyMCk.png" height="80%" width="80%" alt="DHCP"/>
<br />
<br />
Right-click DHCP Relay Agent and select Properties.

 <br/>
<img src="https://i.imgur.com/GynvPMW.png" height="80%" width="80%" alt="DHCP"/>
<br />
<br />
In the Server address field, enter the IP address of the DHCP server. The IP address of the DHCP server I am targeting is 192.168.0.14.
Select Add and then select OK.
 <br/>
<img src="https://i.imgur.com/GEFKCol.png" height="80%" width="80%" alt="DHCP"/>
<br />
<br />
Lastly we verify we're getting an IP address from the DHCP server. I do a quick /ipconfig at the powershell prompt and get an APIPA address. No worries, all I have to do is follow up with a /ipconfig /release & an ipconfig /renew and VIOLA I get a functional IP address.
 <br/>
<img src="https://i.imgur.com/kLulX91.png" height="80%" width="80%" alt="DHCP"/>

<br />
<br />
Lastly we verify we're getting an IP address from the DHCP server. I do a quick /ipconfig at the powershell prompt and get an APIPA address. No worries, all I have to do is follow up with a /ipconfig /release & an ipconfig /renew and VIOLA I get a functional IP address.
 <br/>
<img src="https://i.imgur.com/kLulX91.png" height="80%" width="80%" alt="DHCP"/>

 
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
