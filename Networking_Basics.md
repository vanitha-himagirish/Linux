# Networking Basics

## Domain Naming System 
- The Domain Naming System (DNS protocol) is intended to map human-readable names to the IP address of a server
- DNS queries are sent to a DNS server and forwarded down the hierarchy until an authoratative response is returned

#### Domain Names
- A domain name is the human-readable mapping of a server's IP address
  - For example, "www.google.com" 
- A domain name is split up into multiple parts or "levels"
  - The highest level is the "root" level - there are only 13 root servers in the entire world.
  - The next level is the top-level domain, or TLD (.com, .org, .edu)
  - Next is the second-level domain - what most people consider to be the name of the website
  - Fourth is the subdomain - this is conventionally www, but can be different if an organization has multiple servers
- Domain names are resolved from right to left

#### Fully-Qualified Domain Names
- A fully-qualified domain name is the entire domain name for a server, consisting of both the domain and subdomain
- A FQDN should include a period at the end of the domain name to represent the root DNS server
  - "www.google.com."

![Image of Domain Name structure](https://love2dev.com/img/domain-name-structure-diagram-1956x936.png)

#### Hierarchical Structure
- The Domain Name System uses a hierarchical structure to resolve DNS queries
- At the very top of the hierarchy, there are the 13 "root" DNS servers
- The next level down is comprised of the top-level domain (TLD) servers - these handle requests for .com, .org, .net, etc.
- Second-level domain servers handle requests for "google", "github", "yotabites", etc.
- The third-level domain is also called the subdomain, and refers to the name of the physical server (typically www)

![Image of DNS Hierarchy](https://www.novell.com/documentation/dns_dhcp/dhcp_enu/graphics/dhc_002a.gif)

#### DNS Resolvers
- When your computer makes a DNS request, you are sending the request to a DNS resolver
- The resolver is responsible for contacting the DNS servers and returning a website's IP address to your computer
###### Iterative Queries
  - The resolver first queries one of the root servers to learn the IP of the appropriate TLD server.
  - Next, the resolver queries the second-level server to obtain the IP of the requested resource
  - The IP is returned to the client and the resource is accessed
###### Recursive Queries
  - The resolver sends the query to a DNS server and expects an IP response or an error message
  - If the DNS server does not know the IP address of the requested resource, the server queries other servers on behalf of the resolver
 
![Image of DNS query](https://www.cloudflare.com/img/learning/dns/dns-server-types/recursive-resolver.png)

#### DNS Zones
- The DNS system is broken up into different zones, each managed by an administrator or organization
- A DNS zone always starts at a domain name and can be extended into subdomains 
  - A subdomain may have its own DNS zone if it is complex enough to require separate management
- DNS zones are configured using text files containing DNS records

  
 ![Image of DNS Zones](https://www.cloudflare.com/img/learning/dns/glossary/dns-zone/dns-zone.png)
  
###### DNS Records
 - Zone files must start with a Start of Authority (SOA) record, which contains contact information for the administrator
 - "A" records point a subdomain to an IP address
    - Using the @ symbol in place of the subdomain sets the default IP address for the zone
 - CNAME records point a subdomain to another domain
    - Commonly used to provide naming conventions to users
 - MX records are used to direct email to a mail server
    - The value for this record must be the domain name of a mail host
 - TXT records contain additional notes about the domain
    - Domain name ownership can be verified by adding TXT records to the zone
 - NS records identify authoritative nameservers for the domain
    - These are the servers that contain information about your domain and provide that information to the internet






