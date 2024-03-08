<h2>Generate and Capture Traffic</h2>

<h3>Objectives</h3>
- Establish access credentials on a public RADIUS server.
<br />
- Verify authentication process and security measures.
<br />
- Examine packet data and decrypt password.
<br />
- Conduct comprehensive analysis of authentication process.

<h3>Step 1: Create Username and Password on Public Server</h3>
First, I set up a username and password in plain text on one of the free RADIUS servers available publicly. This step is crucial as it allows me to capture and analyze the traffic effectively. 
<br />
<br />
<img src="https://github.com/Yagoobz/GenerateAndCaptureTraffic/assets/145611184/4ab263ae-caf6-4d3f-89ba-02dc8a59b0e9" height="30%" width="70%" alt="Disk Sanitization Steps"/>

<h3>Step 2: Send Authentication Request to Public Server</h3>
I used a tool called NTRadPing to check if I could access the public server. With the details I got from the RADIUS website, like the IP address, port number, username, and password, I sent a request. It worked! I got access. Then, just to test, I tried using a wrong password. NTRadPing couldn't get a response, showing the security in action.
<br />
<br />
<img src="https://github.com/Yagoobz/WindowsDefenderFirewall/assets/145611184/87b92962-7af3-437d-b223-ee207ec87040" height="30%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
Then, just to test, I tried using a wrong password. NTRadPing couldn't get a response, showing the security in action.
<br />
<br />
<img src="https://github.com/Yagoobz/WindowsDefenderFirewall/assets/145611184/60495eb8-4e0b-46a3-8137-21e19f44f658" height="30%" width="70%" alt="Disk Sanitization Steps"/>

<h3>Step 3: Investigate Packet and Decrypt Password </h3>
When dealing with RADIUS, it's important to note that it doesn't encrypt all traffic. Upon examining the initial request, we can observe the username I transmitted to the server. However, it's worth mentioning that the password remains concealed, ensuring a level of security.
<br />
<br />
<img src="https://github.com/Yagoobz/WindowsDefenderFirewall/assets/145611184/68e07d7a-dd9d-4e81-98d8-18f5eee70a59" height="30%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
To decrypt the password, I navigated to the Protocols tab within the Preferences section of Wireshark and selected RADIUS. Utilizing the shared "secret" password provided by the NTRadPing application, I entered it into the designated field. Boom! The decrypted password appeared in clear-text, allowing for further analysis.
<br />
<br />
<img src="https://github.com/Yagoobz/WindowsDefenderFirewall/assets/145611184/eacbe87d-6836-4069-ac87-8f6b27e8fa6c" height="30%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://github.com/Yagoobz/WindowsDefenderFirewall/assets/145611184/17f7c351-7279-4821-9384-bf7520bc856c" height="30%" width="70%" alt="Disk Sanitization Steps"/>

Alongside the false password, the decrypted credentials were revealed, facilitating a comprehensive analysis of the authentication process.
<br />
<br />
<img src="https://github.com/Yagoobz/WindowsDefenderFirewall/assets/145611184/a15f1a98-9b2b-47f8-935a-d57ef26be834" height="30%" width="70%" alt="Disk Sanitization Steps"/>
