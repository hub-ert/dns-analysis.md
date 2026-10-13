# dns-analysis.md
# DNS Query Analysis with Wireshark

## Objective
What did I want to investigate?
I wanted to capture DNS traffic using Wireshark

## Tools
Which tools and commands did I use?
Windows Command Prompt - to run commands
nslookup - used to send DNS queries
Wireshark - used to inspect and capture DNS traffic
Command: nslookup tryhackme.com 1.1.1.1
## Method
How did I capture and filter the traffic?
I used DNS display filter to show DNS queries and responses.

## Findings
- Queried domain: tryhackme.com
- DNS server: 1.1.1.1
- Transport protocol: UDP (User datagram protocol)
- Query source port: 63951
- Query destination port: 53
- Transaction ID: 0x0004
- Returned IPv4 addresses: 64.239.123.65

## Issues and Troubleshooting
What problems did I encounter?
The default DNS server did not respond to my queries. I queried
1.1.1.1 instead and received a response.

I also noticed that a DNS query included the suffix .telenet.be.
I added a trailing dot to the domain name in the nslookup command
to prevent the suffix from being appended.


## Conclusion
What did I learn?
I learned how to capture DNS traffic and match a query with its
response using the transaction ID, IP addresses and ports.

The capture confirms that the DNS server returned an IPv4 address
for tryhackme.com. It does not prove that the website was reachable
or working correctly.
