# DevOps

## Networking recap

### LAN vs WAN

Local Area Network vs Wide Area Network

LAN: Network that connects computers in a limited area. (e.g.: Wi-Fi, Ethernet)

WAN: Network spanning over long distances. Used to connect LANs or other networks with each other. (e.g.: the internet)

### Subnet

Any subdivison of an IP Network. (e.g.: 10.0.1.0/24 is a subnet of 10.0.0.0/16)

### Public vs Private IP Addresses

Private IP Addresses may only be used internally in a private network. They cannot access the internet directly.

The following ranges are reserved for private IP addresses:

| Class | Address range                 | default subnet mask |
|-------|-------------------------------|---------------------|
| A     | 10.0.0.0 - 10.255.255.255     | 255.0.0.0           |
| B     | 172.16.0.0 - 172.31.255.255   | 255.255.0.0         |
| C     | 192.168.0.0 - 192.168.255.255 | 255.255.255.0       |

Public IP Addresses are unique and are able to connect to the internet.

The gateway (router/modem) owns a public IP address and assigns all computers in his private network a private address (using DHCP).

If a device in a private networks wants to access the internet the private address needs to be translated into a public address first. This is done by the gateway using NAT. The gateway also translates public addresses to private ones, if a device in a private networks wants to recieve data from the internet.

Public and private addresses are also called: external and internal addresses.

### DNS

DNS (Domain Name System) is mainly used to resolve domain names (e.g.: orf.at) to IP addresses.

There are 3 DNS servers: root, domain and authoritative name server.

To resolve a query the request first goes through a root server. 
The root server looks at the domain (e.g.: *.at) at forwards the query to the responsible top level domain server. 
The top level domain server then forwards the query to the authoritative name server, which is responsible for the specific domain (e.g.: orf.at).

### DNS Records

#### A record

Resolves a domain name to an IPv4 address.

#### AAAA record

Resolves a domain name to an IPv6 address.

#### CNAME record

Resolves a domain name to another domain name (e.g.: aliases).

#### MX (mail exchanger) record

Resolves a domain name to the corresponding email server for that domain.

Usually a MX record has 2 entries. 
A primary and secondary mail server.

Each record has a priority number. The lower priority number indicates the primary mail server.

#### SOA (start of authority) record

Stores information about a DNS zone. (zonename, administrator email, serial number (version number))

#### NS (name server) record

Provides the name of the authoritative name server for a domain ("3rd step" of a DNS query).

Usually has 2 entries.
A primary and a secondary name server.

#### SRV (service) records

Resolves a domain name not only to a name of a server, but also to the corresponding port number of a specific service.

#### PTR record

Resolves a IP address to a domain name.