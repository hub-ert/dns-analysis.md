# TCP Three-Way Handshake Analysis

## Objective
Observe how a TCP connection is established.

## Tools
- PowerShell
- Wireshark

## Findings
- Transport protocol: TCP
- Server IP address: 64.239.123.1
- Client source port: 60260
- Server destination port: 443
- Handshake sequence: SYN → SYN-ACK → ACK

The server replied from port 443 to the client's port 60260.
The final packet from the client had the ACK flag set and
the SYN flag unset.

## Conclusion
I identified a complete TCP three-way handshake.
Unlike TCP, UDP does not require a connection handshake before
sending data. My earlier DNS query used UDP, although DNS can
also use TCP.

A successful TCP handshake does not prove that the website
is working correctly.
