[//]: # (Created by Chaz Davis on 2020-02-11)
# Chapter 7 research

# 1.   What types of packets are commonly used for flooding attacks?
Types of packets:
ICMP
UDP
TCP SYN
# 2.   What is “backscatter traffic?” Which types of DoS attacks can it provide information on? Which types of attacks does it not provide any information on?
# 3.   Define a distributed denial-of-service (DDoS) attack.
Denial of service attack is a malicious attempt by an indovidual or group of people to attack any network or website and abrupt the service for the people who are using those network or webistes

it prvents the authorized use of networks, systems or applications with the help of resources such as memory, bandwidth, CPU and disk space.

# 4.  Considering your answer from question 3, is a normal DoS attack from a small number of hosts effective in today's bandwidth heavy networks?  Why or why not?
# 5.   Define a reflection attack.
The sttacker sends the network packet with a spoofed source address to service runs on the network server and the server responds back to this packet by sending it to the spoofed address that belongs to authentic attack target. this is referred to as reflection attack
* i the attacker sends multiple numbers of requests attached all with same spoofed source addresses to the number of servers
* * the the resulting flood of responses for that requests devastates the targets network link it is the fact that the normal server systems used with intermediaries and if the handling of packets is entirely predicatable then these attacks are easier to deploy and harder to trace back to the actual attacker.
# 6.   Define an amplification attack.
Amplification attack is different from the reflector attack and it is used to transmit a packet with spoofed source address to the target system through mediators
* After transmission, it generates multiple responses for each original packet transmitted and it is acheived by sending the original eqiest to some other network by broadcasting the address.
* Finally, the host on the entire network responds to the request and generates a huge number of responses
* alternatively it uses sevice called DNS which generates a longer response than the original request
# 7.   What is the primary defense against many DoS and DDoS attacks, and where is it implemented?
the main critical component of dos attack is the use of spoofed source addresses
the spoofed addresses either difficult to understand the originating system of direct and distributed dos attacks or it is used to direct the reflected or amplified traffic to the target system
so, it is recommended to liit the ability of systems to send the packets with spoofed source addresses
### implementation
the spoofed address filetering must be implemented and needs to be done close to the source paclet with the help of routers or gateways by identifying the valid address range of incoming packets
normally, this is the ISP that provides the network connection for an organization or users from home
ISP knows which address belongs to which customers
Therefore, it is best to ensure whether all the packets from the customers use valid source addresses
# 8.   What defences are possible against a DNS amplification attack? Where must these be implemented? Which are unique to this form of attack?
# 9.   What measures are needed to trace the source of various types of packets used in a DoS attack? Are some types of packets easier to trace back to their source than others?
there are various measures used to trace the source of various types of packets used in the DOS attack:
the organization may wich to ask the ISP to trace the flow of packets to identify the source
if the packets are used with spoofed addresses then it is difficult and time consuming to trace back the packets whereas if they are used with nonspoofed addresses then it is easy to identify the source

are packets easier to trace back:
no! traversing is neither easy nor automated to trace back the source of various types of packets than other packets. this requires cooperation from the network providers to traverse these packets.
# 10.  Is it always possible to trace the general geographic source of a DDoS attack?  
 
