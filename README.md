# Contiki-OS-with-Python-Server-communication

This project provides communication between contiki os and python. As is known, it provides data exchange between border router cooja and external network. A socket listening operation is performed on the source with python jrc.py. In cooja, socket programming is performed for cc2530dk platform.

contiki / examples / cc2530dk / udp-ipv6 / under the udp-client.c file and contiki / examples / ipv6 / rpl-border-router / under border-router.c files are compiled and run in the cooja emulator. The most important condition for data transfer between client and border-router is the ip address in the python socket section. As seen, tunslip

sudo ./tunslip6 -a 127.0.0.1 -p 60001 fd00 :: 5/64

It is run with the command. It should be noted that prefix starts with fd00. If the tuninglip is opened differently, the prefix set cannot be transmitted. We can easily see this in wireshark. For this, please install the Wireshark program and examine the data packages.
