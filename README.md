<p align="center">
 <img src="https://i.imgur.com/cLOWZFd.jpg" height="80%" width="80%" alt="VM logo"/>
</p>

<h1>Creating an IP reservation</h1>


<h2>Description</h2>

Welcome to another setup demonstration! Today, we'll be showcasing how to set up a DHCP relay - a powerful tool that simplifies network management and eliminates the need for multiple DHCP servers. Imagine you have a DHCP server in one part of your network, but your devices are scattered across different networks. Without a DHCP relay, those devices won't be able to obtain an IP address from the server. However, with a DHCP relay, you can easily forward the requests from devices on different networks to the server, and relay the server's response back to the devices. This not only streamlines the IP address assignment process, but also helps centralize the management of your network. So if you're looking for an effective way to optimize your network management, a DHCP relay is definitely worth considering.
<br />

<h2>Environments Used </h2>

 <b>Windows Server 2019 </b> <p>
 <b>Hyper-V</b></p>

<h2>Program walk-through:</h2>

<p align="center">


<br />
From the Hyper-V manager, Select your host server. In this example we will highlight ours which is CORPSERVER. Next we will double-click our DHCP server to connect to the VM.
 <br/>
<img src="https://i.imgur.com/xuHGUAu.png" height="80%" width="80%" alt="DHCP"/>
<br />
<br />
Once our DHCP VM connects. Open server manager then select tools> DHCP
 <br/>
<img src="https://i.imgur.com/hm0Nh6l.png" height="80%" width="80%" alt="DHCP"/>
<br />
<br />
On the left plane expand your domain > IPV4 > Scope

 <br/>
<img src="https://i.imgur.com/30UkFYa.png" height="80%" width="80%" alt="DHCP"/>
<br />
<br />
Right-Click Reservations and select new reservation.
<br/>
<img src="https://i.imgur.com/KsxGpCc.png" height="80%" width="80%" alt="DHCP"/>
<br />
<br />
In the Reservation name field, enter a reservation name
In the IP address field, enter the IP address for the reservation.
In the MAC address field enter the MAC address of your device.
Under supported types select DHCP only. When you are done select Add to create the client reservation.
Select Yes to the DHCP prompt.


 <br/>
<img src="https://i.imgur.com/mS0hoQR.png" height="80%" width="80%" alt="DHCP"/>
<br />
<br />
 That's it! We are finished! You will now see the completed reservation for our device.
 <br/>
<img src="https://i.imgur.com/SO3clD9.png" height="80%" width="80%" alt="DHCP"/>
<br />
<br />
 I hope you enjoyed this demonstration.
 <br/>
<img src="https://i.imgur.com/yJKNCtj.jpg" height="80%" width="80%" alt="DHCP"/>
<br />
<br />

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
