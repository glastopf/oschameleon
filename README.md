![tests](https://github.com/mushorg/oschameleon/actions/workflows/test.yml/badge.svg)

OSChameleon
===========

**OS Fingerprint Obfuscation for modern Linux Kernels.**
*Author: Anton Hinterleitner is111012\@fhstp.ac.at*

Description: Fools the probes of nmap scanner

Prerequisites:

- Linux (tested with Debian/Ubuntu 18.04)
- Python 2.7+
- python-nfqueue=0.6 (apt-get install python-nfqueue)
- requirements.txt

Recorded logs are stored to `/var/log/honeypot/`

Usage:

    python2.7 oschameleonRun.py
        --template path to the nmap fingerprint, either absolute or relative to the execution folder  the iptables to access over ssh. the ssh port should either be changed to 63712 or the port number in stack_packet/helper.py
        --public_ip either fetches the server public ip or gets the ip set for the interface 
        --interface the network interface
        --debug debugging output

**Note: This script flushes iptables before and after usage!**
