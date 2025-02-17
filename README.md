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
<br>


<h2> Step 3 -- Create LimaCharlie Detection Rules</h2>
<p>Creating Detection Rules helps LimaCharlie know what to look for on the target machine! On the LimaCharlie home screen navigate to Automation and then D&R</p> <br>

<img width="661" alt="Detection Rule Lima Charlie Pt 1" src="https://github.com/user-attachments/assets/1856cd0f-d718-4b3a-a9ac-3525507cffe3" />
<img width="677" alt="DetectionRule Lima Charlie Pt 2" src="https://github.com/user-attachments/assets/75a1420c-9112-4c1b-868d-3b92c225e422" />
<br> <br>

These rules look for a new or existing process that: 

 - Contains a windows operating system AND

 * Any of these other conditions:
 * 
 - The File Path ends in Lazagne.exe
 - Command line ends with "all"
 - Command line contains "LaZagne"
 - The binary hash is '3cc5ee..." (seen in picture) 


<h2> Step 4 -- Create LimaCharlie Detection Rules</h2>
<p>Creating Detection Rules helps LimaCharlie know what to look for on the target machine! On the LimaCharlie home screen navigate to Automation and then D&R</p> <br>

<img width="661" alt="Detection Rule Lima Charlie Pt 1" src="https://github.com/user-attachments/assets/1856cd0f-d718-4b3a-a9ac-3525507cffe3" />






