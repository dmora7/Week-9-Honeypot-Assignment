# Week 9 Lab - Into The Packets
## Milestone 0: Networking Toolbox
### Networking Config
Run ifconfig/ipconfig/ip and determine the name/id of your primary network interface?
What is your primary interface's IP address? Is it different from your public IP? Why or why not?
What is the MAC address of your primary interface?
Identify and understand your loopback interface

### Ping
What is the IP address of codepath.com?
What is the IP address of google.com?
Why would the IP address of google.com change between runs or from different locations?

### nslookup
Using the IP for codepath.com from the previous, pass it to nslookup
Does the domain returned from nslookup match? If not, why not?

### traceroute
Compare the traceroutes for codepath.com and google.com
How many of the hops are the same? What accounts for this?
Which has more hops? What accounts for the difference?

### Telnet
What's one thing that makes telnet insecure?
Can you telnet to codepath.com? What port is open and why?

### cURL and wget
Identify some differences between the two
Which would you be more likely to use for interacting with a RESTful API from the command line?
Which support recursive downloading?
Which are you more likely to find pre-installed on a Linux OS?
What is the syntax for each for downloading a file to the current directory?

### ssh and scp
Why is key authentication preferred to passwords?
What is the syntax for copying a file from a local folder to a remote one?

## Milestone 1: Security-Flavored Net Tools
Run nmap against your localhost IP to see all open ports
See how many of the ports you can match to services
Hint: try shutting down Docker or Virtualbox and re-running nmap

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

