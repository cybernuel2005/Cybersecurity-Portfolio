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

#### A Record
These records resolve to IPv4 addresses, for example 104.26.10.229

#### AAAA Record
These records resolve to IPv6 addresses, for example 2606:4700:20::681a:be5

#### 
