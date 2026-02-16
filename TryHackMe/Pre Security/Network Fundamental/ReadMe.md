## What Is Networking - 13-02-2026
A network simply means devices that are connected
- A private Network - Network only allowed users can use
- A Public Network - Network anyone can use

The Internet - One giant network that consists of many small networks with itself
- ARPANET - First internet in the late 1960s, funded by the United States Department of Defense
- World Wide Web(WWW) - A big part of the internet now, invented by *Tim Berners-Lee* in 1989

## IP Address & MAC Address - 14-02-2026
### IP Address
Internet Protocol (IP) Address - A logical address or digital home address assigned to a device for network communication over the Internet.
- Allows devices to send and receive data across networks
- Follows a set of standards called Protocols
- Changes from device to device
- Two devices can't have the same ip address at the same time

The two Types
IPv4:
- Divided into 4 sets of numbers called Octet
- Each section ranges from 0 - 255
- Each octet/section is separated by a dot
- Uses 32-bit, that's 2^32 producing 4.3 billion unique addresses
- Format - 192.168.1.1

IPv6:
- Uses 128-bit, that's 2^128 producing 340 undecillion unique addresses
- Format - 2001:0db8:85a3:0000:0000:8a2e:0370:7334

Private IP Address
- Used within a local network
- Assigned by your network (router, WiFi, internal network carrier)

Public IP Addresses
- Used directly on the internet
- Assigned by your Internet Service Provider (ISP)

### MAC Address
Media Access Control (MAC) Address - A unique permanent ID number given to a device's network hardware to identify a device on a local network
- A device fingerprint
- Made up of 12 characters
- Letters and numbers from 0 - 9 and A - F respectively
- The characters are written in pairs
- Each pair is separated by a colon, considered as seperators
- The first six characters represent the company that made the network device
- The last six characters are unique for devices to devices
- Can be faked or spoofed in the process of spoofing

To apply this concept practically, I completed a Simple MAC Address spoofing:

- Blue ball wasn't allowed to access the TryHackMe site before it's MAC address is blocked
![First step](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/efcafbd20aed865074d59679336ace149fad0061/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-14%20205643.png)
![Second Step](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/1ffbfbee3ff2b853656eb7ceefcbd4c22706c700/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-14%20205522.png)

- MAC Address spoofed To Access the TryHackMe Site
![Third Step](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/a25bdf56500cd14146385ae78b6c7ccc5f6686e4/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-14%20205830.png)
  
## Ping - 15-02-2026
Ping is a command that uses ICMP(Internet Control Message Protocol) packets to determine the performance of a connection between devices over a network or the internet
- Check if a device or website is alive on a network
- The syntax is
  ping id address or website URL

To apply this concept practically, I completed a ping command process

![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/fa5b56433cb3fdc69240e5b912372a373a169def/TryHackMe/Pre%20Security/Network%20Fundamental/Images/Screenshot%202026-02-14%20221017.png)
  
### Go Back
[Pre Security](https://github.com/cybernuel2005/Cybersecurity-Portfolio/tree/main/TryHackMe/Pre%20Security)

