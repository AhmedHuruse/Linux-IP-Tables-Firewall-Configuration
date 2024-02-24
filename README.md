<h1> 🔥 Linux FireWall Config - IP Tables</h1>


<h2>Description</h2>
This projects explains the process in which network packet traffic is managed and configured. IP Tables is broken down into three essential tables. The Filter Table, the Nat Table, and the Mangle Table. The Filter Table, which is responsible for filtering incoming and outgoing traffic, can be further broken down into three chains which are the input, the output and the forward chain. The Filter Table will be the main focus of this project because it deals with Firewall configuration. The chains within the filter table are each responsible for processing packets based on their type. The input chain processes packets that are being sent to the target server. The output chain processes packets that are leaving the server. The forward chain processes packets that are being forwarded from on host to another host using your computer as an intermidiary. The FireWall rules either accept, reject, or drop a packet. Accept means the service or packet can arrive at its destination. Reject means it is blocked from arriving at its target destination and the server administrator is notified of this. Drop means that the connection is simply dropped like it never happend and no one will be notified. Any output also must have specifications. You can block a connection from happening if its does not use a specified protocol like ssh or https.
<br />


<h2>Utilities Used</h2>

- <b>Linux CLI</b> 


<h2>Environments Used </h2>

- <b>Linux Xubuntu</b> (64bit)

<h2>Program walk-through:</h2>

<p align="center">
Launch default filter table that have default policies: <br/>
<img src="https://i.imgur.com/m9Qa3k7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Set the rule to reject all connections from ip address 10.0.0.1 to the target :  <br/>
<img src="https://i.imgur.com/SnQhgZO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In order to delete a rule, you must first use the line-numbers command to assign numbers to the rules. To delete them, simply use the -D command and specify the chain and line number: <br/>
<img src="https://i.imgur.com/rUH2G8c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure rule to reject any incoming connection via SSH to port 22 of the target:  <br/>
<img src="https://i.imgur.com/zXlICND.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure rule to reject any outgoing connections to any ip address that services HTTPS:  <br/>
<img src="https://i.imgur.com/r1bJ4ji.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
