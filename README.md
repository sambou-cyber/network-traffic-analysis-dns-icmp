# Network Traffic Analysis – DNS & ICMP (tcpdump)

This project demonstrates how to analyze DNS and ICMP traffic using the
Linux command-line tool tcpdump to identify why a website could not be reached.

## Summary
Users were unable to access `www.yummyrecipesforme.com` and received a
“destination port unreachable” error.

Packet captures showed DNS queries sent over UDP to port 53 receiving
ICMP error responses indicating the port was unreachable.

## Key Findings
- DNS queries were sent over UDP (port 53)
- ICMP responses returned “udp port 53 unreachable”
- DNS resolution failed due to DNS service unavailability

## Protocols Observed
- UDP (DNS)
- ICMP (Destination Unreachable)

## Root Cause
The DNS service on the destination server was unavailable, misconfigured,
or blocked, preventing DNS resolution.

## Recommended Fix
Restore DNS service availability by ensuring UDP port 53 is open and the
DNS service is running.

## Tools Used
- tcpdump (Linux command-line packet analyzer)
- Linux command line
- TCP/IP networking concepts
