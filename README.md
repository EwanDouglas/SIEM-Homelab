# SIEM-Homelab

<h2>Description</h2>

For this project, I have set up a home lab using Elastic SIEM and a Kali VM. I forwarded data from the Kali VM to the SIEM using the Elastic Beats agent, generated security events on the Kali VM using Nmap, and queried and analyzed the logs in the SIEM using the Elastic web interface. <!-- I also created a dashboard to visualize security events and then created an alert to detect security events and will continue to add more features and dashboards. -->

<br />

<h2>Languages and Utilities Used</h2>

- <b>VirtualBox</b> 
- <b>Elastic Cloud</b> 
- <b>SIEM</b>

<h2>Environments Used </h2>

- <b>Kali Linux</b> 

<h2>Program walk-through:</h2>


Before starting up any virtual machine for the first time, I will tweak my settings to suit my needs and take a screenshot. Every system is different, so be sure to change your settings accordingly. 
<br/>
<img src="https://imgur.com/Ob3adm5.png" height="80%" width="80%" alt="aaa"/>
<br />
<br />
A screenshot will allow us to revert back to this point later on if something goes wrong. Remember to take screenshots often so you don't lose your work!
<br/>
 
<img src="https://imgur.com/ovCHbZe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
The setup is very easy, just select "Graphical Install" and go through the installation steps. Use the default for most settings and check out the online resources if you have any questions! 
  <br/>

<br />
<br />
This is where you will decide your desktop environment, which has a large effect in how your desktop will look and feel. I like xfce but I encourage everyone to experiment!
 <br/>
<img src="https://imgur.com/ppATDFJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 


An agent is a software program that is installed on a device, such as a server or endpoint, to collect and send data to a centralized system for analysis and monitoring. In the context of Elastic SIEM, an agent is used to collect and forward security-related events from your endpoints to your Elastic SIEM instance.
 <br/>
<img src="https://i.imgur.com/XzgluaA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

 
<br />

Here we install the Elastic agent on our Linux VM.
 <br/>
<img src="https://i.imgur.com/c0RU2aE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
We run this command on our Linux machine which shows that the Elastic service is up and running.  
 <br/>
<img src="https://i.imgur.com/G1zJC28.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
We will now run some Nmap scans on the agent to generate activity for our service to recieve. 



  
<img src="https://i.imgur.com/OqeVzwF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Back on the Elastic side we can see the activity that was generated and we can click to find more details about each event.
 <br/>
<img src="https://i.imgur.com/ty84i3C.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />



Here you can see that our SIEM is able to tell us the exact command that was run on the agent machine, in this instance "sudo nmap -sS localhost"
<br/><img src="https://i.imgur.com/OnRGdVt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
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









