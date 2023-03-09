<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- On Azure, ensure that you have a resource group and within that resource group you have a VM titled anything you would like (ex:VMosTicket). As a Side note, you can also title your resource group anything you would like, as well as make your username and password anything easy that you could remember. When it comes down to the size, it would be ideal to at least make the size 2 vcpu's so your virtual machine does not run slow.(there should be a checkbox at the bottom of page when you are done making your username and password, make sure that box is checked)
<img src="https://i.imgur.com/xEzgn7d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
- After Creating your VM, From Azure, copy down the public IP address from the VM and paste it inside of Remote Desktop Connection on your PC and connect to the VM. Remember to type in your unique username and password you made when making your VM
<img src="https://i.imgur.com/D21xbUg.png  height="80%" width="80%" alt="Disk Sanitization Steps"/>
- Inside your VM, right-click the windows icon right next to the search bar click on run and in the search bar type "control" then scroll down to programs click on programs and inside programs click on "turn windows features on or off"
<img src="https://i.imgur.com/AWaK6CZ.png  height="80%" width="80%" alt="Disk Sanitization Steps"/>
- After clicking on "turn windows features on or off" go down to "Internet information services" and make sure that box is filled in. Then from there expand "Internet information services" and go down to World wide web services it should already be filled in, expand that as well. Lastly, expand application development features, go down until you see "CGI" and check the box.
<img src="https://i.imgur.com/emCHmuq.png  height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
