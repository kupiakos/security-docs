---
title: Useful Tools
category: generic
tags: forensics
layout: post
sidebar: true
---

It's always good to know the tools of the trade, but knowing what to use can be hard.
And in the case of Linux, it's nice to know the tools to add in the first place.

_Note that "All" indicates at least recent versions of Linux, Windows, and macOS._

## Recommended Tools for Forensics

Tool | Category | OSs | Description
--- | --- | --- | ---
[Sysinternals](https://docs.microsoft.com/en-us/sysinternals/) | Variety | Windows | Advanced utilities for Windows. Writes to registry on first run.
[Fport](https://www.mcafee.com/sg/downloads/free-tools/fport.aspx) | Network | Windows | Gives PID/process names along with network connections, like Linux `netstat -tualpn`
[Netcat](https://joncraton.org/blog/46/netcat-for-windows/) | Network | All | [See post]({% post_url generic/2018-04-22-netcat %}). Included on most Linux distros by default.
[argus](https://qosient.com/argus/) | Network | Linux | Generates network flow data
[snort](https://www.snort.org/) | Network | Linux | Intrusion Detection System
Netstat | Network | All | Built-in, [Linux post]({% post_url linux/2018-04-22-netstat %}), [Windows post]({% post_url windows/2018-04-22-netstat %})
[Wireshark](https://www.wireshark.org/) | Network | All | Analyze network packets and packet captures
[BIND](https://www.isc.org/downloads/bind/) | Network | All | DNS Tools
[Volatility](https://github.com/volatilityfoundation/volatility) | Memory | All | Extracts digital artifacts from RAM samples
[Rekall](https://github.com/google/rekall) | Memory | All | Memory acquisition and analysis
[VirusTotal](https://www.virustotal.com) | Malware | Web | Anyalyzes suspicious files/URLs for viruses
[REMnux](https://remnux.org/) | Reverse-Engineering | Linux | Toolkit for Reverse-Engineering/Analyzing Malware
[IDA](https://www.hex-rays.com/products/ida/support/download_freeware.shtml) | Reverse-Engineering | All | Interactive Disassembler
[radare2](https://github.com/radare/radare2) | Reverse-Engineering | Linux | Way more advanced GDB
