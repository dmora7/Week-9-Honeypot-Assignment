# Week-9-Honeypot-Assignment
> ## Overview & Setup
In this lab exercise, I used Google Cloud Provider to provision my VMs (Honeypot and MHN Admin). 
1. The first step required the installation of GCP SDK on my local machine to allow the use of `gcloud` from the command line.  
2. Once that was finished installing, I created the MHN Admin VM using `gcloud` and established a SSH connection to verify connectivity. 
3. Next, I was suppose to install the MHN Application onto the MHN Admin VM but I was unsuccessful. It kept giving me an error when running the `sudo ./install.sh` command. It kepy prompting me to enter my github credentials but no matter what I entered, it kept saying the Github directory could not be found. 
4. I was able to move on however and created the Honeypot VM on my cloud provider and established a connection to that VM as well. 
5. Next, the Honeypot VM needed to get the Honeypot Application installed but since I was unable to install the Admin console application, I was unable to access the MHN admin console where the script gets deployed onto the Honeypot VM. 
6. I was still able to run a `nmap` scan on the Honeypot VM but without the Honeypot application, there were no vulnerable ports opened that would attract potential attackers. 

> ## Demonstration
**Milestone 0: To the Cloud!**
<img width="892" alt="30" src="https://user-images.githubusercontent.com/37861847/41143515-6d1a15ce-6aae-11e8-836d-ad97ca369d38.PNG">

**Milestone 1: Create MHN Admin VM**
<img width="865" alt="31" src="https://user-images.githubusercontent.com/37861847/41143527-74d6b24a-6aae-11e8-84b2-0d977a72de08.PNG">

**Milestone 2: Install the MHN Admin Application**
<img width="895" alt="32" src="https://user-images.githubusercontent.com/37861847/41143538-7ba37d60-6aae-11e8-8fa3-2e9bb51c2d91.PNG">

**Milestone 3: Create a MHN Honeypot VM**
<img width="863" alt="33" src="https://user-images.githubusercontent.com/37861847/41143545-81c57fae-6aae-11e8-812f-3f123cbd225b.PNG">

**Milestone 5: Attack!**
<img width="849" alt="34" src="https://user-images.githubusercontent.com/37861847/41143554-8822bdee-6aae-11e8-87c1-2cce4a0799b0.PNG">

> ## Review 
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
