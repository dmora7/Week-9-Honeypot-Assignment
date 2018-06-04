# Week-9-Honeypot-Assignment

### Which Honeypot(s) did you deployed?

<img width="613" alt="googlemachines" src="https://user-images.githubusercontent.com/37861847/40894819-f5e99060-6760-11e8-9277-61f5392184e1.PNG">

I was able to configure both VMs on my google cloud platform but unfortunately, I have not been able to deploy my Honeypot. When installing the MHN admin application on the remote VM, I can not get bypassed this error that prevents me from installing the Honeypot application onto the Honeypot VM. 

<img width="490" alt="errorlab9" src="https://user-images.githubusercontent.com/37861847/40894109-0f97daa8-675c-11e8-80d3-b9809374671d.PNG">

Therefore, I currently have both VMs up and running and are accessible through their external IPs but there is no Honeypot application (Ubuntu - Dionaea with HTTP) installed on the virtual machine. 

### Any issues you encountered?
Yes and in specific, installing the MHN Admin application on the remote machine. I was able to clone the github repository given in the instructions but when running the install script, it will prompt me halfway through the installation to enter a github username and password. After many trials, I was not able to get bypass this error and avoiding me to install the application which allow access to the MHN Admin console via the browser. 

### A summary of the data collected: number of attacks, number of malware samples, etc.
I was not able to conduct any scans or obtain information about any attacks. I was able to run a `nmap` scan on the HoneyPot's external IP but since the honeypot application was not installed, the only port that was open was port 22 (SSH). 

### Any unresolved questions raised by the data collected?
I did not have access to the admin console and the UI so no data was able to be collected.

### Additionally, include a json export of the data you collected in the repo, instructions for which can be found in the next section.
N/A
