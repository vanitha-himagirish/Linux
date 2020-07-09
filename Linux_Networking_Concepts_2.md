
Firewall

A firewall is a network security device that monitors incoming and outgoing network traffic and permits or blocks data packets based on a set of security rules. Its purpose is to establish a barrier between your internal network and incoming traffic from external sources (such as the internet) in order to block malicious traffic like viruses and hackers.
Firewalls carefully analyze incoming traffic based on pre-established rules and filter traffic coming from unsecured or suspicious sources to prevent attacks. For Example:  Firewall rules can be "Source address 172.18.1.1 is allowed to reach destination 172.18.2.1 over port 22"
A software firewall is a program installed on each computer and regulates traffic through port numbers and applications, while a physical firewall is a piece of equipment installed between your network and gateway
Packet-filtering firewalls, the most common type of firewall, examine packets and prohibit them from passing through if they don’t match an established security rule set. 
 Stateless firewalls examine packets independently of one another and lack context, making them easy targets for hackers. In contrast, stateful firewalls remember information about previously passed packets and are considered much more secure.
Redhat and CentOS have prebuilt firewalld

Other type of firewalls include Proxy firewalls, NAT(Network Address Translation) Firewalls, NGFW(Next Generation Firewalls) and Stateful Multilayer Inspection Firewalls(SMLI)


IP Address:
An IP address provides an identity to a networked device on the internet that supplies a specific physical location with an identifiable address, devices on a network are differentiated from one another through IP addresses
We can use Ip addr show command to find our IP address.

IPv6(2 to the power 128) is replacing IPv4 is that it provides a larger number of IP addresses than IPv4(2 to the power 32)
There are private IP addresses, public IP addresses, static IP addresses, and dynamic IP addresses.
Private addresses are used in Local Area Networks (LAN). They are bound to a specific network.Public addresses are necessary for establishing external connectivity to other networks, most notably the "Worldwide Web" (www) of the Internet.

I don't think we have enough permissions for checking firewalls and IP changes on user account. Here are some commands we can work
Checking the status of IPTables / Firewall. 
iptables -L -n -v( “-L” (List ruleset), “-v” (Verbose) and “-n” (Displays in numeric format).)
iptables -F  Flushing or deleting IPTables rules
