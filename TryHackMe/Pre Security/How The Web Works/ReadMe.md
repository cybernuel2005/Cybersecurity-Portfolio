## DNS In Detail - 01-03-2026
### What is DNS?
Domain Name System (DNS) is the internet’s "phonebook," translating human-readable domain names (e.g., example.com) into machine-readable IP addresses (e.g., 192.0.2.1).

### Domain Hierarchy
#### Root Domain
Represented by a dot(.).
The root is managed globally by organizations like ICANN(Internet Corporation for Assigned Names and Numbers) and operated by root server operators.
The root servers don’t know every IP address — they only know where to find Top-Level Domains.

#### TLD (Top-Level Domain)
A TLD is the most right-hand part of a domain name. So, for example, the tryhackme.com TLD is .com. 

There are two types
- gTLD (Generic Top Level) - Historically, a gTLD was meant to tell the user the domain name's purpose; for example, a .com would be for commercial purposes, .org for an organisation, .edu for education, and .gov for government. Due to such demand, there is an influx of new gTLDs ranging from .online, .club, .website, .biz, and so many more.

-  ccTLD (Country Code Top Level Domain) - A ccTLD was used for geographical purposes, for example, .ca for sites based in Canada, .co.uk for sites based in the United Kingdom, and so on.

 For a full list of over 2000 TLDs https://data.iana.org/TLD/tlds-alpha-by-domain.txt

 #### Second-Level Domain
 This is what usually means when they say “domain name.”. Taking tryhackme.com as an example, the .com part is the TLD, and tryhackme is the Second Level Domain.
- The second-level domain is limited to 63 characters + the TLD
- Can only use a-z 0-9 and hyphens (cannot start or end with hyphens or have consecutive hyphens(sometimes possible, but there are exceptions)).

#### Subdomain 
A subdomain sits on the left-hand side of the Second-Level Domain using a period to separate it; for example, in the name admin.tryhackme.com the admin part is the subdomain.
- Has the same creation restrictions as a Second-Level Domain, being limited to 63 characters and can only use a-z 0-9 and hyphens (cannot start or end with hyphens or have consecutive hyphens).
- You can use multiple subdomains split with periods to create longer names, such as jupiter.servers.tryhackme.com.
- There is no limit to the number of subdomains you can create for your domain name.
- But the length must be kept to 253 characters or less( including the Subdomain(s), Second-Level Domain, and TLD)

## DNS Records Type - 03-03-2026
DNS records are instructions stored in a domain’s DNS zone that tell the internet how to handle traffic for that domain.

##### A Record
These records resolve to IPv4 addresses

##### AAAA Record
These records resolve to IPv6 addresses

##### CNAME (Canonical Name)
These records resolve to another domain name

##### MX Record (Mail Exchange)
These records resolve to the address of the servers that handle the email for the domain you are querying

##### TXT Record
TXT records are free text fields where any text-based data can be stored. 
- Can be to list servers that have the authority to send an email on behalf of the domain (this can help in the battle against spam and spoofed email)
- Can also be used to verify ownership of the domain name when signing up for third-party services.

#### Making A Request
What happens when you make a DNS Request
- Local cache check - Your computer first checks its local cache to see if you've previously looked up the address recently.  if not, a request to your Recursive DNS Server will be made.
- Recursive DNS server -  Usually provided by your ISP, but you can also choose your own. This server also has a local cache of recently looked up domain names. If a result is found locally, this is sent back to your computer, and your request ends here. If the request cannot be found locally, a journey begins to find the correct answer, starting with the internet's root DNS servers.
- The root DNS server - Acts as the DNS backbone of the internet; their job is to redirect you to the correct Top Level Domain Server, depending on your request. If, for example, you request www.tryhackme.com, the root server will recognise the Top Level Domain of .com and refer you to the correct TLD server that deals with .com addresses.
- The TLD server -  Holds records for where to find the authoritative server to answer the DNS request. The authoritative server is often also known as the nameserver for the domain.
- The authoritative DNS server - Is the server that is responsible for storing the DNS records for a particular domain name and where any updates to your domain name DNS records would be made. Depending on the record type, the DNS record is then sent back to the Recursive DNS Server, where a local copy will be cached for future requests and then relayed back to the original client that made the request.
 
NOTE: DNS records all come with a TTL (Time To Live) value. This value is a number represented in seconds that the response should be saved for locally until you have to look it up again. Caching saves on having to make a DNS request every time you communicate with a server.

### Practicals
![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/80a6a86052754c312fb41423be282e5c56056c86/TryHackMe/Pre%20Security/How%20The%20Web%20Works/Image/Screenshot%202026-03-03%20084539.png)

![](https://github.com/cybernuel2005/Cybersecurity-Portfolio/blob/09b91002e4b735d00a80905a105d2473d9c7e10c/TryHackMe/Pre%20Security/How%20The%20Web%20Works/Image/Screenshot%202026-03-03%20085743.png)
