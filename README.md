# On-Premises-Active-Directory
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />




- 

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create a Resource Group for the Domain Controller and Client One VM's
- Create the Domain Controller Server
- Create the  Client One Virtual Machine
- Ensure Connectivity between DC-1 and Client-1 VM's

<h2>Deployment and Configuration Steps</h2>

<p>
<<blockquote class="imgur-embed-pub" lang="en" data-id="a/VDjGtGP" data-context="false" ><a href="//imgur.com/a/VDjGtGP"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>
</p>
<p>
Go to portal.azure.com, Go to resources and create a new resource, It should go through the review and create process. When done,Go to virtual machines and create a new virtual machine ( server). MAke sure to give DC-1 4 cpu's or it will run slowly.Click next until you get to networking and create a new Virtual Network. Click next until you get to review and create and deployment is complete. Create Client 1's virtual machine. Select the same resource group you selected for DC-1. YOu cam make 2 cpu's for this virtual machine. Click next until you get to networking and type in the same resource you created for DC-1 should pop up. Click next until get to review and create. The Deployment process may take a while to complete.
</p>
<br />

<p>
<https://imgur.com/JaIJpek
</p>
<p>
Install Active Directory by logging into DC-1 with your username and password you created at the creation of the Server. IF the credentials work. You should be able to log into Remote Desktop. If you're not sure which virtual machine you're using. Go to the search bar ar the bottom left of the screen. Type in Command Prompt and open it up. Type in "whoami" and you will know,which virtual machine you're using. Close command prompt when you're done using it. 
</p>
<br />

<p>
<<blockquote class="imgur-embed-pub" lang="en" data-id="a/QoEBqqd"  ><a href="//imgur.com/a/QoEBqqd">IPv4 ping</a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>
</p>
<p>
To ensure connectivty between Client One and the Domain Controller. Login to Client One's virtual machine with Remote Desktop. Use the credentials you saved when creating Client One's virtual machine. YOu can type cmd which is Command Prompt in the search bar. Type in ping-t and the Private IP address for DC-1. If it times out, habe to go to windows firewall advanced and enable all the Ipv4 prtocols to ensure connection between the DC-1 and Client one virtual Machines. 
</p>
<br />
