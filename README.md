# SOAR-EDR

<img width="573" alt="Screen Shot 2025-02-17 at 6 53 05 AM" src="https://github.com/user-attachments/assets/a5a821d3-473e-46f6-9fe9-e345d73e033f" /> <br>

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
   
 - The File Path ends in Lazagne.exe
 - Command line ends with "all"
 - Command line contains "LaZagne"
 - The binary hash is '3cc5ee..." (seen in picture)
<br> <br>


<h2> Step 4 -- Run Lazagne on Virtual Machine and discover Credentials </h2>
<p>LaZagne is used by Digital Forensic Professionals, Pen Testers and Bad Actors</p> <br>


<img width="982" alt="LazagneExecution" src="https://github.com/user-attachments/assets/ba68c5da-a3ca-4e6f-b016-3af88a481b84" />

<img width="1037" alt="LazagneCredentialsRevealed" src="https://github.com/user-attachments/assets/644125ee-de9e-4053-93da-ca419996b6ec" />



h2> Step 5 -- When Lazagne Runs on our Virtual Machine, LimaCharlie alerts our Automation program Tines </h2>
<p>Tines then sends out a Slack Message and Email with details about the alert</p>

<img width="1026" alt="SlackDetailMessage" src="https://github.com/user-attachments/assets/58d973e2-859f-4127-a47e-6b8ac49d57c7" />  <br>

<img width="733" alt="Screen Shot 2025-02-15 at 1 10 22 PM" src="https://github.com/user-attachments/assets/d981051d-cc8b-4801-9148-82e8a5cc0d32" />
<br> <br>



h2> Step 6 -- A User Prompt is sent to the user asking if they want to isolate the endpoint </h2>

<img width="390" alt="UserPrompt" src="https://github.com/user-attachments/assets/6ce364dc-eac1-48bd-9287-81d011c50cfb" />


h2> If the User decides to Isolate the Endpoint then LimaCharlie will Isolate it from the network </h2>

<img width="448" alt="ComputerIsolated" src="https://github.com/user-attachments/assets/161c32a6-6406-4ead-89e3-75a9545f236c" /> <br>


<p>Before Removing our virtual machine from the Network we can ping websites from Powershell in our Windows VM</p> <br>
<img width="1096" alt="PingSuccessful" src="https://github.com/user-attachments/assets/a1b45777-b595-400d-89c4-dcec3d68600c" />


<p>After Removing our virtual machine from the Network we can no longer ping any websites! </p> <br>
<img width="1085" alt="PingFailureafterisolation" src="https://github.com/user-attachments/assets/cfc16024-47cc-40c1-87de-428e8a6dc580" />


h2> A Final Slack & Email Message is Sent Confirming the Isolation of that endpoint/machine </h2>
<br>
<h2>Slack Machine Isolation Message Confirmation</h2>
<img width="830" alt="SlackIsolationEmail" src="https://github.com/user-attachments/assets/a26c9bea-67c6-4471-af2e-56c2bc7c5be0" />

<br>
<h2>Email Isolation Message Confirmation </h2>
<img width="740" alt="ComputerIsolationEmaill" src="https://github.com/user-attachments/assets/41a75f89-f6e4-473a-97de-9979ab56da9b" />


<h2>Final Takeaways</h2>

<P>How cool is it to be able to isolate a machine! In the real word this is extremely important to be able to stop malware/ransomware or any other malicious program from spreading throughout the network. It is almost like removing cancer from the body before it can spread!</P>

