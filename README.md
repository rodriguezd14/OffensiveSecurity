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

Code behind phishing attack

<img width="987" height="323" alt="image" src="https://github.com/user-attachments/assets/96fa9124-68d0-4e98-a63d-28ab1b906e65" />


Phishing email harvesting credentials

<img width="477" height="310" alt="image" src="https://github.com/user-attachments/assets/4a3ac0e1-f73a-4811-915b-c4093b19ba78" />



Backend

<img width="475" height="112" alt="image" src="https://github.com/user-attachments/assets/9eac0a0d-dbcc-45b5-bce2-73021d548845" />



Cloning website

<img width="972" height="315" alt="image" src="https://github.com/user-attachments/assets/74ae43f6-b584-4e6d-a291-7ce9bd93621b" />




