# Networking Activities Lab 2 (Configuring a Firewall)
This lab kicks off a demo series of my networking and remote desktop skills. I use Microsoft Remote Connection to observe ICMP traffic between two Azure VMs. Using PowerShell, I ping one VM from the other and monitor the ICMP packets with Wireshark.


<h2>Programs, Languages, and Utilities Used</h2>

- <b>Microsoft Azure</b> 
- <b>Powershell</b>
- <b>Wireshark</b>

<h2>Environments Used </h2>

- <b>Windows 11</b> (23H2)

<h2>Program walk-through:</h2>

<p align="center">
Initiate a perpetual/nonstop ping from the Windows 11 VM to the Ubuntu VM using code: ping [IP Address] -t  <br/>
<img src="https://i.imgur.com/XLitHiN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In Azure navigate to the Linux VM and go to Networking--> Network Settings--> and click the Network Security Group link <br/>
<img src="https://i.imgur.com/NRx3Kxj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Navigate to Settings--> Inbound security rules--> and click Add <br/>
<img src="https://i.imgur.com/sP6W8Cm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Click the ICMPv4 option under Protocol and ensure all other settings are exactly as they are in the image below and then click "Add" <br/>
<img src="https://i.imgur.com/pN9Laso.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Go back into the Windows 11 VM, and observe that in Powershell the requests will begin to perpetually time out. Also, note that in Wireshark the ICMP traffic only shows requests from the Ubuntu VM and no longer shows replies coming from the Windows 11 VM<br/>
<img src="https://i.imgur.com/WnLlXjw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Once you delete the rule from the "Inbound security rules" you can go back into Wireshark and Powershell and see how they have been reverted back to their original state <br/>
<img src="https://i.imgur.com/16Fk8VH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/e1g98bE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
To finish the lab, use command "Ctrl+C" in Powershell to stop the ping and click the red square icon in Wireshark to "Stop" the ICMP traffic information <br/>
<img src="https://i.imgur.com/fqo0p6p.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
