# Offensive Seucrity Project
**HomeLab Environment**

The purpose of this homelab environment is to demonstrate a Phishing attack with a keylogger script being deployed
to an enterprise environment. The homelab contains opnsense router and Windows Server along with a Windows Client and Ubuntu Server that
are both connected to the domain associated with the Windows Server running Active Directory service. OPNsense
acts as a router with two interfaces one connected to the ISP and the other connected to a network switch. Along side
OPNsense a Windows Server machine is deployed to run a DHCP server and Active Directory, this is accomplished by configure
DHCP Relay on OPNSense and DNS query forwarding. 



**Network Layout (Subnet 192.168.1.0/24):**
- OPNSense Router (IP Address 192.168.1.1): Redirects packets accross different networks and connects devices to internet connection from ISP
- Windows Server (IP Address 192.168.1.2):  Runs DHCP and AD
- Windows Client (IP Address 192.168.1.4):  Windows machine for Active Users to login
- Ubuntu Server (IP Address 192.168.1.5):   File Server that is connected to the domain using Samba and realm

nmap scan of every ip address on the network that has open ports
```
nmap -sS 192.168.1.0-6
```
<img width="1168" height="785" alt="Screenshot 2026-04-01 113312" src="https://github.com/user-attachments/assets/74d73ad1-8ef2-4ee1-8740-6a77748f6201" />

Enumerating ports and Services running on 192.168.1.2
```
nmap -sC 192.168.1.2
```
<img width="869" height="829" alt="Screenshot 2026-04-01 114930" src="https://github.com/user-attachments/assets/3b109f65-30ab-4ad9-9c00-440ce162d1a8" />


