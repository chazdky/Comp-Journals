[//]: # (Created by Chaz Davis on 2020-02-11)
Chapter 6 research
Same directions as usual

# 1.   Briefly describe the four generations of anti-virus software.
anti-virus: The computer software that is used to avoid, catch, and eliminate malicious software is known as anti-virus
Four generations:
first generation anti-virus software needs a "Simple scanners" to determine the malware
second gen avs needs a "Heuristic scanners" to search for possible malware occassion using heuristic rules or needs an "integrity checking" to determine changed files
third gen avs needs "Activity traps" in an infected program to determine malware by its measures rather than its structure.
fourth gen avs needs "Full Featured Protection" This full featured protection uses a collecion of anti-virus techniques packages used in conjunction with activity trap components and scanning.
# 2.  Describe some malware countermeasure elements.
prevention: this measure prevents malware from getting into the system or blocking its capability to change the system through policy, awareness, susceptibility, mitigation, and threat detection
detection: the measure determines the positions of the malware
Identification: detects the specific malware that has infected the system
Removal: removes all elements of malware vires from evenry infected system so it cannot propAGATE FURTHER.
# 3.   What is the difference between a backdoor, a bot, a keylogger, spyware, and a rootkit? Can they all be present in the same malware?
Backdoor: it is a secret admission point into a system or program that permits an important person who is concious of the backdoor to get access without going through the common security access procedures
Rootkit: collection of programs implenented on a system to sustain secret access to that system with administrator rights, whilehiding proof of its precense to the most extent possible
Bot: a threat to the network resources and computational of the infected system for use and it is done by the attacker
keylogger: software which records every keystroke on the infected machine to permit an attacker to observe responsive information especially the information that contains the login and password credentials
spyware: an attack that causes the machine to permit observing of a hge range of action on the system, observing the history and content of browsing action, dynamically changes the data exchange between the browser and websites

Yes, all can be present within the same malware.
# 4.  What is "Ransomware"?
a type of malicious software designed to block acces to a computer system until a sum o money is paid. files are encrypted. like an RSA encryption, where the attacker has the unencryption and until paid you are locked out.
# 5.   What means can a worm use to access remote systems to propagate?
the mechanisms that worm can use to spread:
Email or instant messenger
file sharing
remote execution capability
remote file access or trasfer capability
remote login capability
# 6.   Assume you have found a USB memory stick in your work parking area. What threats might this pose to your work computer should you just plug the memory stick in and examine its contents? In particular, consider whether each of the malware propagation mechanisms we discuss could use such a memory stick for transport. What steps could you take to mitigate these threats, and safely determine the contents of the memory stick?
when a memory stick is plugged into the computer which was found in the parking area may create a variety of threats to the confidentiality, integrity, and availability of the system
the memory stick may transmit "Executable virus" or "macro virus" on to the system
Executable virus - Executable program files are affected by machine executable virus and these program files work with specific operating system and in some cases it is based ipon the hardware platform.
macro virus - Files with macro or scripting code are affected by macro viruses and its suport effective content in a field of user documen types and is translated by an application
the memory stick may transmit a "malicious worm"
Worm - While viewing the memory stick, worm runs automatically and infects other approriate files as a virus on the system
the memory stick may contain a trojan orse
trojan horse - malicious piece of code that is delivered through the mail or web page or through the USB drives that causes damage to the data or system
Therefore, "Executable virus" "Macro virus" "worm" and "Trojan horse" are hte threats that are created to the user's computer when a memory stick is plugged in

Steps to mitigate the problem:
the user should scan the memory stick with appropriate up-to-date avs
the user could check the memory stick in a controlled environment. for example a live boot linux or emulation environment
therefore these are the steps to mitigate the threats

# 7.   Consider the following fragment:
legitimate code
if data is Friday the 13th;
crash_computer();
legitimate code
What type of malware is this?
The type of malware being used is a logic bomb. Logic bomb is a key part of data corrupting malware.
* it is code inserted in malware that is placed to "explode" when certain actions are met
* The actions take place in the given fragment, it checks the data with appropriate day and date that is Friday the 13th
* if the condition is met it calls the function crash_computer()
* for a logic bomb, the example conditions hat can be used as triggers are as follows
* the presence or absence of devices or files on the system
* an appropriate date or day of the week
* software with appropriate version or configuration
* the application executed by the appropriate user
* once activated, a bomb may change or delete data or complete files, or other damage
