Linux is one of the most popular choices for running web servers and applications. This also makes it a high-value target for hackers. A number of security breaches have been the result of improper application of security controls, or un-patched Linux operating systems. Research different security breaches to Linux systems, what lead to the exploitation, and how the hack could have been prevented.

By Thursday, create a thread minimum 200 words summarizing your research, citing at least two sources (Wikipedia is a weak source, find another.)

By Sunday, reply to at least two classmate's threads with minimum 100 words.

## Dubsmash

### Date: December 2018

### Impact: 162 million user accounts

Details: In December 2018, New York-based video messaging service Dubsmash 
had 162 million email addresses, usernames, PBKDF2 password hashes, and 
other personal data such as dates of birth stolen, all of which was then 
put up for sale on the Dream Market dark web market the following December. 
The information was being sold as part of a collected dump also including 
the likes of MyFitnessPal (more on that below), MyHeritage (92 million), 
ShareThis, Armor Games, and dating app CoffeeMeetsBagel.

Dubsmash acknowledged the breach and sale of information had occurred — and 
provided advice around password changing — but failed to say how the 
attackers got in or confirm how many users were affected.

## My Fitness Pal

### Date: February 2018

### Impact: 150 million user accounts

Details: As well as Dubsmash, UnderArmor-owned fitness app MyFitnessPal 
was among the massive information dump of 16 compromised sites that saw 
some 617 million customers accounts leaked and offered for sale on Dream Market.

In February 2018 the usernames, email addresses, IP addresses, SHA-1 and 
bcrypt-hashed passwords of around 150 million customers were stolen and then 
put up for sale a year later at the same time as Dubsmash et al. MyFitnessPal 
acknowledged the breach and required customers to change their passwords, 
but didn’t share how many accounts were affected or how the attackers gained 
access to the data.

## Zynga

### Date: September 2019

### Impact: 218 million user accounts

Details: Once a giant of the Facebook gaming scene, Farmville creator Zynga is 
still one the biggest players in the mobile game space with millions of players 
worldwide.

In September 2019, a Pakistani hacker who goes by the name Gnosticplayers 
claimed to have hacked into Zynga's database of Draw Something and Words with 
Friends players and gained access to the 218 million accounts registered there. 
Zynga later confirmed that email addresses, salted SHA-1 hashed passwords, 
phone numbers, and user IDs for Facebook and Zynga accounts were stolen.


# “Seems like a hell of a lot of effort; it must have been a target of real #
# interest” #

A sophisticated hacker group pwned Amazon Web Services (AWS) servers, set up a 
rootkit that let them remotely control servers, then merrily funnelled 
sensitive corporate data home to its command and control (C2) servers from a 
range of compromised Windows and Linux machines inside an AWS data centre.

That’s according to a report from the UK’s Sophos published late last week, 
which has raised eyebrows and questions in the security industry. The attackers 
neatly sidestepped AWS security groups (SGs); which, when correctly configured, 
act as a security perimeter for associated Amazon EC2 instances.

The unnamed target of this attack had correctly tuned their SGs. But with a 
rootkit installed on their AWS servers that gave attackers remote access, 
the compromised Linux system was still listening for inbound connections on 
ports 2080/TCP and 2053/TCP: something that eventually triggered Sophos’ 
intervention.

# AWS Servers Hacked But “It Could Have Been Anyone”

Sophos was at pains to emphasise that while this particular attack targeted 
AWS servers, it was “not an AWS problem per se. It represents a method of 
piggybacking C2 traffic on a legitimate traffic… in a way that can bypass 
many, if not most, firewalls.”

Security experts agreed that the attacker, likely a nation state actor, 
could have used the bespoke rootkit to funnel data off most servers, 
whether in the cloud or on-premises. (Those interested in the precise 
details of how the attackers managed their data exfiltration can refer 
to detailed technical write-up here).

Sophos dubbed the incident, which used a customised Gh0st RAT trojan 
– ”Cloud Snooper”. One cybersecurity researcher (initial reaction: 
“dude this happens all the time. It only gets noticed if it has a fancy name”) 
described it to us after looking closely at the incident as 
“from a technical perspective, a thing of beauty…

Many questions about the security breach remain unanswered, however, 
not least how the attackers got the rootkit onto the AWS servers to start with.

## Here’s What Happened

Sophos said: “An analysis of this system revealed the presence of a rootkit 
that granted the malware’s operators the ability to remotely control the 
server through the AWS SGs. But this rootkit’s capabilities are not limited 
to doing this in the Amazon cloud: It also could be used to communicate with, 
and remotely control, malware on any server behind any boundary firewall, 
even an on-premises server.

“By unwinding other elements of this attack, we further identified other 
Linux hosts, infected with the same or a similar rootkit.

The company added: “Finally, we identified a compromised Windows system 
with a backdoor that communicated with a similar C2 as other compromised 
Linux hosts, using a very similar configuration format. The backdoor is 
apparently based on source code of the infamous Gh0st RAT malware.”

At the heart of the attack was another backdoor trojan 
dubbed “snoopy” that can be executed both as a command line tool and as a 
daemon. This opens HTTP and/or DNS services on a compromised system, and 
allows traffic tunneling, operating both as a reverse SOCKS5 proxy server, 
and client.

[//]: # "Snoopy stores many debug messages in clear text, several in Chinese, i.e. “远程内存空间分配失败! – Remote memory space allocation failed!”"

# Sophos’s full write-up of the techniques used can be found here [pdf].

“The default installation for the SSH server also needs extra steps to harden it”
The security firm noted: “AWS SGs provide a robust boundary firewall for EC2 
instances. However, this firewall does not eliminate the need for network 
administrators to keep all external-facing services fully patched.

“The default installation for the SSH server also needs extra steps to harden 
it against attacks, turning it into a rock-solid communication daemon.”

Security researcher Willem Mouton told Computer Business Review: 
“From a technial perspective it is a thing of beauty, also the 
fact that they made it cross platform.

“The one thing that the article did not clear up was what the initial 
entry vector as well as the privacy escalation was. In order to install 
such a rootkit you would probably [need] root on Linux and 
LocalAdmin/System level privileges on Windows.

“This rootkit was most probably deployed to maintain an advanced 
covert level of network persistence. Which makes me wonder on whose 
network they found this because that seems like a hell of a lot of 
tech and effort so it must have been a target of real interest. Also, 
the article mentions everything was hosted on AWS, and usually 
you would see attackers go for the AWS/Cloud tenancy or subscription to maintain access, but again nothing of that was mentioned.

“I would love to see the full outcome of their investigation”.

Sophos said Indicators of Compromise (IoCs) included having the following ports open on local host: tcp 2080; udp 2053; tcp 10443. Suspect file names include /tmp/rrtserver-lock; /proc/sys/rrootkit; /tmp/rrtkernel.ko; /usr/bin/snd_floppy; snd_floppy.

The following warning syslog messages also showed up:

- “…insmod: ERROR: could not insert module /usr/bin/snd_floppy: File exists”
- “…kernel: snd_floppy: loading out-of-tree module taints kernel.”
- “…kernel: snd_floppy: module verification failed: signature and/or required key missing – tainting kernel

One high profile previous attack on cloud servers was demonstrated by Eclypsium, which leased a bare metal IBM server and exploited a vulnerability in its Baseboard Management Controller (BMC); a third-party server component used to enable remote management for initial provisioning, OS reinstall and troubleshooting.

It then relinquished the use of the server, which was re-released for use by other cloud customers. But the BMC was not re-flashed with factory firmware meaning Eclypsium sustained its access, in an incident that IBM Cloud played down.



# Amazon Capital one

Amazon is at least partly blame for the massive 2019 Capital One breach that impacted more than 100 million customers, senators are alleging. Security researchers however are of two minds.

In a letter to the Federal Trade Commission (FTC) this week, U.S. senators Ron Wyden (D-Ore.) and Elizabeth Warren (D-Mass.) called for the investigation of Amazon’s role in the Capital One data breach, where a hacker accessed data that was hosted on servers on Amazon’s cloud-based computing platform, Amazon Web Services (AWS).

“Amazon knew, or should have known, that AWS was vulnerable to server-side request forgery [SSRF] attacks,” the senators wrote on Thursday. “Although Amazon’s competitors addressed the threat of SSRF attacks several years ago, Amazon continues to sell defective cloud computing services to businesses, government agencies, and to the general public. As such, Amazon shares some responsibility for the theft of data on 100 million Capital One customers.”

SSRF is a type of server attack where servers can be tricked into connecting to another server it did not intend to. SSRF flaws occur when an online application requires outside resources enabling an attacker to send crafted requests from the back-end server of a vulnerable web application.

In the case of the 2019 breach, a misconfigured web application firewall, which was hosted on the AWS cloud platform, enabled a hacker to launch the SSRF attack and access credit applications, Social Security numbers and bank account numbers between March 19 and July 17. The illegally accessed data was primarily related to credit-card applications made between 2005 and early 2019, by both consumers and businesses. These include a raft of personal information, such as names, addresses and dates of birth; and financial information, including self-reported income and credit scores.

Because other Amazon competitors have built protections against SSRF into their products – including Google since 2013 and Microsoft since 2017 – part of the blame for the attack rests on AWS for not building in similar protections, said the senators: “The FTC has the authority and responsibility to investigate unfair and deceptive business practices. We urge you to investigate whether Amazon’s failure to secure its services against SSRF attacks constitutes an unfair business practice, which would violate Section 5 of the FTC Act,” they said.

The letter has split the security community between those who say that Capital One should bear more responsibility in securing its cloud configurations for platforms that host its customer data – and those who say that the onus rests on Amazon to build in more protections to its own product. Some security experts are dismissing the letter altogether, saying that it demonstrates a lack of understanding by politicians of how cloud services work.

“Amazon did not a rent a server to Capital One in the sense that this was a compromised managed server,” Chris Morales, head of security analytics at Vectra, told Threatpost. “There might be confusion and a lack of understanding on how to properly configure privileged access authentication tokens which is a feature of AWS. An analogy would be blaming an apartment complex owner if a tenant of that apartment complex was robbed. That is not something that is enforced today either.”

Security in the cloud is a shared responsibility, but it’s “squarely up to the enterprise” when it comes to determining who has privileges for impacting cloud infrastructure, Balaji Parimi, CEO at CloudKnox Security said in an email: “There are tens of thousands of configurations and privileges within AWS and other cloud platforms, and it only took one such overprovisioned role to lead to the Capital One breach,” he said.

Others, like Evan Johnson, manager of the product security team at Cloudflare, argue that major cloud players hold some level of responsibility in ensuring that their products protect against common attacks like SSRF. That could include bundling protections into AWS like requiring a special header for metadata service requests or requiring temporary credentials to be used in the correct virtual private cloud (VPC).

“The impact of SSRF is being worsened by the offering of public clouds, and the major players like AWS are not doing anything to fix it” Johnson said in an August post. “In my opinion, it’s clear that AWS’ product offering is not complete since this is a major and recurring problem amongst their biggest customers. AWS should do something about this because IAM [identity and access management] is the root of all security within AWS.”

AWS did not respond to a request for comment from Threatpost. However, Amazon said issued a media statement to CNBC:

“The letter’s claim is baseless and a publicity attempt from opportunistic politicians. As Capital One has explained, the perpetrator attacked a misconfiguration at the application layer of a Capital One firewall. The SSRF technique used in this incident was just one of many subsequent steps the perpetrator followed after gaining access to the company’s systems, and could have been substituted for a number of other methods given the level of access already gained.”

The hack was one of the biggest data breaches to ever hit a financial services company — putting it in the same league in terms of size as the Equifax incident of 2017. The FBI arrested a suspect in the case: A former engineer at Amazon Web Services (AWS), Paige Thompson, after she boasted about the data theft on GitHub.

Capital One for its part in July said it had fixed what it called a “configuration vulnerability” and that it is “unlikely that the information was used for fraud or disseminated by this individual” — though investigations are ongoing.


https://www.cbronline.com/news/aws-servers-hacked-rootkit-in-the-cloud
https://www.csoonline.com/article/2130877/the-biggest-data-breaches-of-the-21st-century.html

https://news.sophos.com/wp-content/uploads/2020/02/CloudSnooper_report.pdf
