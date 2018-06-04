# Week 9 Lab - Into The Packets
## Milestone 0: Networking Toolbox
### Networking Config
**1. Run ifconfig/ipconfig/ip and determine the name/id of your primary network interface?** _eth1_

**2. What is your primary interface's IP address? Is it different from your public IP? Why or why not?** _192.168.33.15_

**3. What is the MAC address of your primary interface?** _08:00:27:af:30:9a_ 

**4. Identify and understand your loopback interface.** _127.0.0.1 The loopack address is a virtual network interface that your computer uses to communicate with itself._

### Ping
**1. What is the IP address of codepath.com?** _198.58.125.217_

**2. What is the IP address of google.com?** _216.58.193.206_

**3. Why would the IP address of google.com change between runs or from different locations?** _Google deals with millions of requests at any given time and to be able to faciliate that service to end users, Google has many data centers located around the world that host the application. Each data center has a unique public IP address that is accessible. Therefore,the IP addresses of each data-center are added to the DNS entry of google.com. Resulting in different IP addresses being associated with google.com._

### nslookup
**1. Using the IP for codepath.com from the previous, pass it to nslookup**

<img width="299" alt="nslookup" src="https://user-images.githubusercontent.com/37861847/40581689-b2f2673a-6113-11e8-964e-87d4673b6213.PNG">

**2. Does the domain returned from nslookup match? If not, why not?** _Yes, it matches._

### traceroute
**1. Compare the traceroutes for `codepath.com` and `google.com`.**

<img width="366" alt="traceroute" src="https://user-images.githubusercontent.com/37861847/40896246-bd0098cc-6768-11e8-84c3-593c9198c09f.PNG">

**2. How many of the hops are the same? What accounts for this?**
_Both hops are the same because in order to reach the destination whether it be codepath.com or google.com, the hops in between are both the same when running traceroute from the same location. Of course, they may differ in other situations as discussed earlier with google.com having many servers.


### Telnet
**1. What's one thing that makes telnet insecure?** _Telnet sends packet information in clear text that is able to be sniffed by a man in the middle attack that will expose sensitive information._

**2. Can you telnet to codepath.com? What port is open and why?** _Yes, you can telnet to codepath.com on port 22 which is listening for incoming ssh connections._

### cURL and wget
**1. Identify some differences between the two** _wget is more simple and straightforward to use and doesn't require a library to run. It's meant for quick downloads and not much more. cURL on the other hand is powered by a library, libcurl, and it can do a lot more than download content from the internet. cURL supports a wide variety of protocols in comparison to wget._

**2. Which would you be more likely to use for interacting with a RESTful API from the command line?** _cURL_

**3. Which support recursive downloading?** _wget_

**4. Which are you more likely to find pre-installed on a Linux OS?** _wget_

**5. What is the syntax for each for downloading a file to the current directory?**

### ssh and scp
**1. Why is key authentication preferred to passwords?** _Key authentication is more secured than using passwords which can be easily guessed. In addition, passwords have the concern of having botnets guessed usernames and passwords resulting in the system's logs getting clogged. Key authentication however has more possible combinations making it harder to guess and requires a copy of a legitimate private key that corresponds to a public key stored on the server. Therefore, key authentication mitigates the possibilty of guessing usernames and passwords._

**2. What is the syntax for copying a file from a local folder to a remote one?**

_scp `filename` user@xx.xx.xx.xx:/destination/path_

## Milestone 1: Security-Flavored Net Tools
**1. Run nmap against your localhost IP to see all open ports.**
<img width="364" alt="nmap" src="https://user-images.githubusercontent.com/37861847/40600060-d112d64a-6204-11e8-9907-cb165026451b.PNG">


**2. See how many of the ports you can match to services.**
`Hint: try shutting down Docker or Virtualbox and re-running nmap`
After shutting down Vagrant, the only port open remained the port displayed above. 

## Milestone 2: Grabbing Packets with tcpdump
**Challenge 1:** Determine the IP address for `codepath.com` and use `tcpdump` to display packets with that IP as the destination. Then open http://www.codepath.com in the browser and check the output. Notice the output displays the HTTP requests in addition to the packets.

How many requests to load the main codepath.com page?
What type of resource accounts for most of the requests?
Now try the same exercise with https://security.codepath.com. What differences do you see in the output? What accounts for those differences?

**Challenge 2:** You can also monitor DNS queries on port 53 with tcpdump. Use this to determine the IP of your primary DNS:

Listen for DNS queries on port 53: sudo tcpdump -vvv -s 0 -l -n port 53
Think of a domain name that probably exists (common word or phrase + .com) but that you've never visited before (suggestion: zombo.com) and open it in a browser
Look at the tcpdump output for the UDP packets trying to resolve the domain. The destination IP should be the DNS

## Milestone 3: Hello, Wireshark
**Challenge:** Get a capture of the baseline traffic on your wireless interface. Start by closing every running app on your system: every window, every tab, every shell...try to go completely dark (restart your system first if you need to). Then open Wireshark (which should be the only app running) and start capturing on your primary interface.

Look at the source and destination IPs; how much of the traffic is inbound vs. outbound?
Try `nslookup` on a couple of IPs that aren't in your network. See if you can figure out who those IPs belong to
Try to identify traffic associated with at least one process on your host that's either part of the OS itself or is auto-launched at startup
See if you can spot any ARP packets used to resolve IPs to MAC addresses

## Milestone 4: Traffic Analysis — Mike's Computer is Acting Weird
just submit screenshots 

## Milestone 5: Traffic Analysis — Mystery Meat Malware
more screenshots

## Milestone 6: Wi-Fi Hacking — Crack a Handshake
**Challenge:** Crack a WPA2 handshake
screenshots

## Milestone 7: Wi-Fi Hacking — Grab a Handshake
**Challenge:** 
What is the protocol of the handshake packets?
Where is the SSID?
Where specifically is the hash?
What is a nonce?

