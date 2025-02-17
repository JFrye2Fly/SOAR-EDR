# SOAR-EDR

In this project I build a <b>SOAR (Security Orchestration and Automated Response)</b> tool with <b>Tines</b> (Automated Workflow builder) and with <b>LimaCharlie</b> as the EDR (Endpoint Detection Response) tool. 
<br />

<br>
<h3>Languages and Utilities Used</h3>

- <b>Vultr.com</b> -- Launching a Windows[Uploading EDR&SOAR.drawio…]()
 Server/Virtual Machine
- <b>Tines</b> -- An automnation platform 
- <b>Lima Charlie</b> (EDR & Versatile Security Monitoring Tool) 
- <b>Lazagne</b>-- An open-source credential harvesting tool which gathers credentials from browsers, databases and more.
<br>


<h2> Step 1 -- Build A WorkFlow Diagram </h2>
<h3>Everything starts when LimaCharlie detects a malicious program on our computer! The malicious program in this case is LaZagne. Eventually A User Prompt is given to isolate the machine and Email/Slack messages with more detail are sent.</h3><br>

<img width="655" alt="Screen Shot 2025-02-16 at 2 59 40 PM" src="https://github.com/user-attachments/assets/1c4e96d6-4d0f-44aa-9bdb-58699373b4b2" />


<h2> Step 2 -- Install a Lima harlie Agent on the Windows Virtual Machine</h2>
<h3>This will allow LimaCharlie to detect and report any suspicious activity and get our automated workthrough started</h3>h3>

The command to install the agent is comprised of the <strong><LaZagne executable/strong>, -i character and CharlieLima sensor Id. 
<img width="1077" alt="InstallingLazagne" src="https://github.com/user-attachments/assets/0be7423d-620d-4849-9df7-0ba13a6d1ecc" /> <img width="572" alt="InstallingLazagne2" src="https://github.com/user-attachments/assets/08cb18c1-6194-400f-9863-2e19d499b63a" />

<h2> Step 3 -- Install...</h2>
<h3>Step 3...</h3>

The command to install the agent is comprised of the <strong><LaZagne executable/strong>, -i character and CharlieLima sensor Id. 
<img width="1077" alt="InstallingLazagne" src="https://github.com/user-attachments/assets/0be7423d-620d-4849-9df7-0ba13a6d1ecc" /> <img width="572" alt="InstallingLazagne2" src="https://github.com/user-attachments/assets/08cb18c1-6194-400f-9863-2e19d499b63a" />


<p align=left> After launching the virtual machine "TPOT" in the Azure Cloud many malicious hackers 
began their attempts to hack the virtual machine. This a live attack map. As you can see countries from all over the world tried to exploit this vulnerable VM.</p>

<img src="https://i.imgur.com/enpYnkf.jpg"/>

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
