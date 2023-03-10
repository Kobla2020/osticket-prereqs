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
</p>
<p>
After registering the new PHP version, you download osTicket, after downloading osTicket, you open the osTicket file folder and there should be two folders inside that read "scripts" and "upload". In a seperate file explorer app, go into the Windows (c:) and go to the folder that reads "inetpub" and open it up. After opening the inetpub folder, open up the wwwroot folder that should be at the bottom. Next you would drag the upload folder that was downloaded inside of the osTicket folder inside of the wwwroot folder and rename the upload folder "osTicket". If you dont have it open already, open IIS as an administrator and restart the page again.
</p>
<br />

<p>
<img src="https://i.imgur.com/uwTpfHn.png"  height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside of IIS, on the far left side you should see the name of your VM. click the down arrow to expand the options, now you should see "Application pools" and right below that, you should see "sites". Click the arrow to expand "sites". Now you should see "Default website", expand that as well. Lastly, you should see the "upload" folder you renamed to "osTicket" click on that then on the far right hand side of IIS you should see something that says "browse *80:(http)". After clicking on that, it should open up an osTicket page in your browser.
</p>
<br />

<p>
<img src="https://i.imgur.com/HhdIXI8.png"  height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
As you open the osTicket page in the browser, you should notice that some of the features have an "x" and some have a check mark next to them. We need to change some of those "x's" to a checkmark. In order to do that, we need to go back into IIS then go into the PHP manager. after going into PHP manager, scroll all the way to the bottom until you see an option that says "PHP Extensions" then right below that it should say "enable or disable an extension", click on that. After going inside "enable or disable an extension", there are 3 features that we need to enable and they are: PHP_IMAP, PHP_INTL, PHP_OPCACHE. they should all be disabled, click on each one and on the right hand side of IIS it should have something that says "Actions" and underneath of it, you should be able to enable each of the extensions. After enabling the extensions, go back to the browser and refresh the osTicket page and you should notice some of the options that had an "x" previously next to it now have a checkmark.
</p>
<br />

<p>
<img src="https://i.imgur.com/Vm2QhtF.png"  height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now you want to go back into file explorer and open up the Windows (c:) and go into the "inetpub" folder. after opening the inetpub folder, go into the "wwwroot" folder then open the "osTicket" folder which was formerly named "upload". After opening the osTicket folder, you should see a large amount of files. There should be a file that says "include" click on that and scroll near the botom of the "include" folder there should be a file that reads "ost-sampleconfig.php". Rename the ost-sampleconfig.php folder to "ost-config.php". After renaming the folder, right click it then click on properties. there should be some tabs on the top. Click on the tab that reads "security" and inside of the security tab it should have an option to look at the advanced settings, click on "advanced". After clicking on advanced, it should open up a new window and near the bottom of the window, there should be an option that reads "Disable inheritance" after clicking on that it should ask you what you would like to do with the inherited permissions, after seeing this click on the option that says "Remove all inherited permissions from this object". Now where it used to say "disable inheritance" now says "enable inheritance" and right above that, it says "add". Click on where it says "add" then click "select a principal" which should be near the top on the right hand side of the screen. Where it says "enter the object name to select" type "everyone" then press "Ok". Now where it says "basic permissions", fill in the box where it says "full control" then press "ok" at the bottom right hand side of the window then when that window closes, click on "apply" on the next window and then click "ok" then click "ok" again on the last window.
</p>
<br />

<p>
<img src="https://i.imgur.com/8yIkrnL.png"  height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we're finally getting to osTicket! on the browser page, click continue and fill in the credentials. Make sure to fill your username and password in with something that you will remember.
</p>
<br />

<p>
<img src="https://i.imgur.com/ZGW1RUM.png"  height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
At the bottom of the osTicket page in the browser, you should notice it has some prompts that ask you to enter: MYSQL USERNAME, MYSQL PASSWORD, MYSQL DATABASE. You should already know your "MYSQL password" because when we downloaded MYSQL earlier you made your MYSQL password but now we need to get your MYSQL username and database. Now you would need to download and install "Heidi SQL" after the installation, it should open up a new window and near the bottom left hand side of the window it should say "new", click on that and you should see a prompt where it says "user" then to the right of that it says "root" that is your "MY SQL username" and where it says "password", enter your password that you made when downloading MYSQL earlier. Now click on open at the bottom. There should be a rectangular shaped window to the left of the Heidi SQL window and inside of that window it reads "unnamed", Left click on unnamed and then click on the option that says "create new" then on the next mini window, it should say database which should be the only option that is not greyed out, click on that and type "osTicket" inside the bar. Now we have the username, password and the database. User is "root", Password is the password you made from earlier and the database is "osTicket". When you type all that in, click "install", and we finally installed osTicket!
