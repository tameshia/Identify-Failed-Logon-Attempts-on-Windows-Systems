# Identify Failed Logon Attempts on Windows Systems



<h2>Languages and Utilities Used</h2>

- <b>pending</b> 

<h2>Environments Used </h2>

- <b>Windows Server 2019</b> 


<h2>Lab Description</h2>
  <p>pending </p>
  
 

  <h2>Directions</h2>



<hr>
From taskbar, click the <b>Windows Start</b> icon then click the <b>Event viewer</b> button. <p></p>

![event viewer](https://user-images.githubusercontent.com/107451613/176720521-8e7da4c8-44e9-4948-9167-c77f058f29c4.png)
<hr>
<p>From the left pane, navigate to <b>Event Viewer > Windows Logs > Security </b> to open the Security log in the center pane. The top of the security pane lists the total number of failed and successful logon attempts.</p>

![navigation](https://user-images.githubusercontent.com/107451613/176721970-0d5992e5-020e-4f73-a3df-fbd49357162e.png)
<hr>

<p>On the far right, you will see the Actions pane. Click <b>Filter Current log</b> to open its dialog box. </p>

![filter log](https://user-images.githubusercontent.com/107451613/176723795-93bda28b-0072-4ba8-a225-dd397046aaf0.png)

<hr>

Locate the <All Event IDs> dialog box and type <b>4625</b>. A failed login attempt is given the Event ID of 4625. A complete list of Event IDs can be found <a href="https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/default.aspx"> here </a>. Click <b>OK</b> to apply the filer.</p>

![log4625](https://user-images.githubusercontent.com/107451613/176724604-3d87da87-20a8-4147-b2c4-555f47765214.png)

<hr>
The center of the Event Viewer pane will display all failed logon attempts. If there are an unusually high number of logon attempts within a short period of time, this may suggest an attempted brute force attack. As general rule of thumb, five or more failed logon attempts per account should be investigated. 
<p>Double click on a failed logon attempt. This will display the Event Properties dialog box. This will show details about the time, date, failure reason, and information about the computer that attempted the logon. Pertinent information from this dialog box can be used to investigate the event further. You can see which username the target was trying to logon to (TargetUserName), the IP address where the logon attempt originated, the port used, and the process that initiated the event. 
