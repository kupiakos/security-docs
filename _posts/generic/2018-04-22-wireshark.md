---
title: Wireshark
category: linux
layout: post
---


Wireshark is an incredibly useful Swiss-army knife for packet analysis.
It's available on almost every platform and gets better every day.
It can run on a live system, or perform analysis on a packet capture file.

On top of the obvious, here are some useful functions of Wireshark:

## Statistical Data
This gives us a good overview of what’s going across the network (live) or in the packet capture.
When using Wireshark, open the Statistics menu and then Protocol Hierarchy.
This will breakdown the packets shown in the main window (if there are any filters applied, those will apply to the breakdown too) into the protocols that are used.
It will show the number of packets, bytes, and percentage of the total that is used by each protocol.
Right clicking the protocol and adding a filter will change the main window to only show that protocol.
In Wireshark, you can also open the Statistics menu and then view IPv4 Statistics and Destinations and Ports.
This summarizes traffic to each port and destination IP. It reports the packet count and the percentage of all traffic.
This window also accepts filters just like the main window, allowing the user to narrow down what they’re looking for.
Even more useful, it has the option to export the data to a CSV file, which can then be imported into your favorite spreadsheet editor, and filtered and sorted however desired.

## Conversations
Open the Statistics menu and then select Conversations.
This will output the full list of sessions, at the Ethernet, IP and TCP/UDP level.
There is a checkbox that says, "Limit to display filter" that will filter the results of this window to that of the main window.
The contents of this window can also be exported and filtered/analyzed in your favorite spreadsheet editor.

## Full packet capture
This can take a while to do.
Wireshark is typically the best tool for this, as it allows the user to quickly filter packets, based on almost any value or flag in the packet.
It also comes with the best packet dissection tool, and supports almost any protocol you can throw at it, allowing you to see the meaning behind every packet.
Recent versions of Wireshark even allow you to extract objects from the packet streams, such as files transferred over SMB or HTTP.

## Other useful tools
- View URLS of all HTTP requests in packet capture - Open Statistics menu - HTTP - Requests
- Export Objects sent via HTTP, SMB or TFTP - Open File menu - Export Objects
- Enable/Disable IP to DNS reverse name resolution - Open Preferences, and then Name resolution
- Override protocol decoding for a specific port (this is useful when using non-standard ports, such as HTTP(S) over something other than 80/443) - Right click packet in main window - Decode as...
- View TCP connection as just plain text - Right click packet - Follow TCP Stream

_Note: much of this content is taken verbatim from a separate lab assignment_
