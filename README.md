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
<img src="https://i.imgur.com/xykNeNJ.png  height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The first thing you would need to download for osTicket is "PHP Manager for IIS" without this, we wouldnt be able to enable certain settings that is needed to run osTicket. After the initial download, make sure to double click "PHP Manager for IIS" in your downloads folder to finish the download.
</p>
<br />

<p>
<img src="https://i.imgur.com/9SlCpRD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The next thing you would need to install for osTicket is the "Rewrite module" for both the "PHP manager for IIS" and the "Rewrite Module", you would only need to press next until you get the option to fully install then click install.
</p>
<br />

<p>
<img src="https://i.imgur.com/nuysGcu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now you would need to create the "PHP" file in the C: in your VM. Next, download "PHP 7.3.8" and extract the contents inside of "PHP 7.3.8" into the PHP folder inside of the C: you just made.(It would be easiest to open up another file window while doing this). Right click on the "PHP 7.3.8" file you just downloaded, it should give you an option to "extract all", click on that. After, you would need to click "browse" and go to your Windows (c:) in "This PC" and select the PHP folder you just made.
</p>
<br />

<p>
<img src="https://i.imgur.com/cbAfocr.png"  height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next you would download and install "Redist"
</p>
<br />

<p>
<img src="https://i.imgur.com/zcg0Ldu.png"  height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now you would download "My SQL" and when you are doing the installation process, select "typical setup" and then Install. In the next section, you would select "Standard Configuration" and type in a reliable password that you would remember and then click next and Install.
</p>
<br />

<p>
<img src="https://i.imgur.com/GqC8fUf.png"  height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next you open IIS as an Administrator then go to "PHP manager". Inside there, look at "PHP Setup" and there should be an option underneath that reads "Register new PHP version", select that then a bar should come up with 3 dots on the right hand side of it. The 3 dots basically mean "browse" so you would click on those 3 dots then go into the windows (c:) and click the PHP folder that we made earlier and all the way at the bottom of the folder it should say "PHP-CGI" select that and click "open". After you are finished registering the new php version, go back to the main screen that intially popped up when you ran IIS as an administrator and on the far right hand side, click on the icon that signifies refreshing the page.
</p>
<br />

<p>
<img src="https://i.imgur.com/Dui17En.png"  height="80%" width="80%" alt="Disk Sanitization Steps"/>
