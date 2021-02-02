Ping or Packet Internet Groper is a network management utility that can check the connection status between a source and destination computer/device over an IP network. It also helps you estimate the time it takes to send and receive a response from the network.

We all have our favorite websites that we visit frequently; if one of them doesn’t load, we really want to know why. Is it because we don’t have an Internet connection, or is it problems with our Internet service provider that are preventing us from accessing the website? Another reason could be the unavailability of the website itself. Whatever the reason, the Linux Ping command can give you all the answers.

Ping uses the Internet Control Message Protocol (ICMP) to send and receive echo messages to and from the host or target computers to keep us informed of network performance. An ICMP request message is sent to the target computer; if the target IP address is available, it sends an ICMP message response to the host computer. This informs us about the connectivity status of the network, such as the round-trip time – the time it takes to send and receive an information packet.

**syntax**

```
ping [options]
```

Option|	Description
-------|-----------
a	|Use this option for a beep sound when the peer is reachable
b	|Use this option to allow pinging a broadcast address
B	|Use this option if you do not want to allow the ping to change the source address of the probe
c (count)|	Use this option to set the number of times to send the ping request
d	|Use this option to set the SO-DEBUG option on the socket being used
f	|Use this option to flood the network by sending hundred or more packets per second
i (interval)	|Use this option to specify an interval between successive packet transmissions. The default value of interval is 1 second
I (interface address)	|Use this option to set source address to the specified interface address. This option is required when pinging IPv6 link local address. Its argument can be an IP address or name of the device.
l (preload)	|Use this option to set the number of packets to send without waiting for a reply. For selecting a value more than 3, you need to be a super user.
n	|Use this option to display network addresses as numbers rather than as hostnames
q	|Use this option to display a quiet output. It means that only the summary is displayed at startup and finish time
T (ttl)	|Use this option to set the Time To Live
v	|Use this option for verbose output
V	|Use this option to display the version and exit
w (deadline)	|Use this option to specify a timeout, in seconds, before ping exits, regardless of how many packets have been sent or received.
W (timeout) | Use this option to set the time(seconds) to wait for a response

**Examples**
* ping -i 5 127.0.0.1
* ping ip_address