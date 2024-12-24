<h1>Configuring ASDM</h1>


<h2>TLDR Description</h2>
Configuring ASDM (Adaptive Security Device Manager) on a Cisco ASA 5505 firewall.
<br />

<h2>Purpose</h2>
The purpose of this lab was to set up ASDM (Adaptive Security Device Manager) on our Cisco ASA 5505 firewall to make configuring it a lot more user friendly with the GUI. 
<br />

<h2>Background Info</h2>
Cisco ASA’s offer the use of ASDMs as a way to make client use much easier and cleaner in general, it offers many configuration wizards that are extremely important and used widely throughout the industry. With ASDM configurations that might take an hour or two to finish after collecting all the resources necessary, only take a few minutes if not seconds. It also offers monitoring for the firewall to easily view activity, alongside troubleshooting and other useful tools.
<br />

<h2>Lab Summary</h2>
The configuration of the ASA itself to set up ASDM was fairly simple and only took a little bit to find on google, it consisted of addressing, setting up the https server and setting the username and password of an admin login. The main challenging part of this lab was troubleshooting through the log provided by ASDM to fix the java issue which ended up being a pretty simple fix but was surprisingly difficult to find anywhere online, we had to figure that out on our own by messing with settings in our java settings.
<br />

<h2>Network Diagram</h2>
<p align="center">
  <img src="https://i.imgur.com/pPWMh3n.png" height="40%" width="40%" alt="Network Diagram"/>
</p>
<br />

<h2>Lab Commands</h2>
  -	nameif outside – sets the name of an interface in the firewall.
<br />
  -	http server enable – enables http server into the ASA.
<br />

<h2>Walk-Through:</h2>

<p align="center">
Configuring the vlan and http server for access to the ASDM<br/>
<img src="https://i.imgur.com/2m0EZiJ.png" height="80%" width="80%" alt="ASDM Config Steps"/>
<br />
<br />
Once I accessed the http server I then installed the ASDM launcher and logged into the ASDM using device IP and the username and pass I set in the config above.<br/>
<img src="https://i.imgur.com/puciIz5.png" height="80%" width="80%" alt="http server"/>
<br />
<br />
Here is the ASDM up and running in our environment<br/>
<img src="https://i.imgur.com/Es0IwiZ.png" height="80%" width="80%" alt="ASDM running"/>
<br />
<br />
<img src="https://i.imgur.com/TPGEmWc.png" height="60%" width="60%" alt="Palo Alto Firewall Factory Reset Steps"/>
<br />
<br />
The prompted admin override page that we were looking for, proves filtering and possible admin override is working.<br/>
<img src="https://i.imgur.com/2otyiO4.png" height="80%" width="80%" alt="Palo Alto Firewall Factory Reset Steps"/>
<br />
<br />
</p>

<h2>Problems</h2>
We ran into multiple problems in this lab trying to figure out how to get ASDM up and running, the main problem we had that took us a long time to figure out after endless google searching and messing with settings in java was that java was having a hard time running the ASDM on our computers. We found a fix to this issue by using the bootup log that the launcher has and literally messing with almost all of the java settings to finally find what was wrong which ended up being the TLS certificates.
<br />

<h2>Conclusion</h2>
This lab overall was extremely simple but it took us a very long time to figure out just how simple it was, the process of finding the solution was pretty difficult in itself. It took us a few class periods scavenging google for anything useful and we ended up finding the solution to our java problem through troubleshooting and not even google. After all of that I ended up finally getting ASDM to work and from what I’ve seen from it so far it will probably prove to be very useful in our upcoming labs.
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
