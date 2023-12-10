<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, DHCP, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>Key Steps</h2>

- Observation of ICMP traffic.
- Observation of SSH traffic.
- Observation of DHCP traffic.
- Observation of DNS traffic.
- Blocking certain traffic by configuring Inbound rules.

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/r1RrjQs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  To observe ICMP traffic between Windows and Linux hosts within Wireshark, I first set the filter to show only ICMP traffic.
</p>
<p>
  <img src="https://i.imgur.com/1CXhD80.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Then, I ping my Linux host to test for connectivity, see the traffic produced as a result. 
</p>
<p>
<img src="https://i.imgur.com/f1k5V2N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To observe SSH traffic only between the two hosts, I set the filter to show only SSH traffic.
</p>
<p>
  <img src="https://i.imgur.com/f1k5V2N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
  <img src="https://i.imgur.com/uwvYQ00.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  After utilizing SSH in the Powershell command-line tool, observe SSH traffic between the two hosts.

<br />

<p>
<img src="https://i.imgur.com/LOp90ja.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here, I have configured the network security group settings in Azure to disallow any inbound traffic to my Linux host. Let's test it with Wireshark.
</p>
<br />
<img src="https://i.imgur.com/gZSdbpe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
  As you can see, SSH traffic is now blocked by the firewall.
</p>
<br />
<img src="https://i.imgur.com/ctAh7Vh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
Here, I observe DHCP traffic by using the command-line ipconfig /renew to prompt DHCP requests.
</p>
<br />
<img src="https://i.imgur.com/UXNlOH0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

In this step, I observe DNS traffic by using nslookup to find DNS information from www.target.com.
<p>
  
</p>


