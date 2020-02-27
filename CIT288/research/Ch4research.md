[//]: # (Created by Chaz Davis on 2020-02-06)
Same directions as always.

1.  what is a Trust Framework?  Give at least one real-world example of its use in Microsoft or Linux offerings.

In digital identity systems, a trust framework functions as a certification program. It enables a party who accepts a digital identity credential (called the relying party) to trust the identity, security, and privacy policies of the party who issues the credential (called the identity service provider) and vice versa.


https://www.quora.com/What-is-a-trust-framework?top_ans=637875

2.  Who is OIX?  ICF? ICAM? OITF? OIDF?  What is the mission of each of these?  

OIDF: The OpenID Foundation is an international nonprofit organization of individuals and companies committed to enabling, promoting, and protecting OpenID technologies. OIDF assists the community by providing needed infra- structure and help in promoting and supporting expanded adoption of OpenID.
• ICF:TheInformationCardFoundationisanonprofitcommunityofcompanies and individuals working together to evolve the Information Card ecosystem. Information Cards are personal digital identities people can use online, and the key component of identity metasystems. Visually, each Information Card has a card-shaped picture and a card name associated with it that enable people to organize their digital identities and to easily select one they want to use for any given interaction.
• OITF:TheOpenIdentityTrustFrameworkisastandardized,openspecification of a trust framework for identity and attribute exchange, developed jointly by OIDF and ICF.
• OIX: The Open Identity Exchange Corporation is an independent, neutral, international provider of certification trust frameworks conforming to the Open Identity Trust Frameworks model.
• AXN: An Attribute Exchange Network (AXN) is an online Internet-scale gateway for identity service providers and relying parties to efficiently access user-asserted, permissioned, and verified online identity attributes in high volumes at affordable costs

3.  Explain what an AXN does.  

Subjects: These are users of an RP’s services, including customers, employees, trading partners, and subscribers.
• Attribute providers (APs): APs are entities acknowledged by the community of interest as being able to verify given attributes as presented by subjects and which are equipped through the AXN to create conformant attribute creden- tials according to the rules and agreements of the AXN. Some APs will be sources of authority for certain information; more commonly APs will be bro- kers of derived attributes.
• Identity providers (IDPs): These are entities able to authenticate user creden- tials and to vouch for the names (or pseudonyms or handles) of subjects, and which are equipped through the AXN or some other compatible Identity and Access Management (IDAM) system to create digital identities that may be used to index user attributes.
There are also the following important support elements as part on an AXN:
• Assessors: Assessors evaluate identity service providers and RPs and certify that they are capable of following the OITF provider’s blueprint.
• Auditors: These entities may be called on to check that parties’ practices have been in line with what was agreed for the OITF.
• Dispute resolvers: These entities provide arbitration and dispute resolution under OIX guidelines.
• Trust framework providers: A trust framework provider is an organization that translates the requirements of policymakers into an own blueprint for a trust framework that it then proceeds to build, doing so in a way that is consistent with the minimum requirements set out in the OITF specification. In almost all cases, there will be a reasonably obvious candidate organization to take on this role, for each industry sector or large organization that decides it is appropriate to interoperate with an AXN.

4.  How are capability tickets utilized?

capability ticket A discretionary access control technique organized by subject. For each subject, the capability ticket lists objects and their permitted access rights by this subject.

When it is desired to determine which subjects have which access rights to a particular resource, ACLs are convenient, because each ACL provides the informa- tion for a given resource. However, this data structure is not convenient for determin- ing the access rights available to a specific user.
Decomposition by rows yields capability tickets (see Figure 4.2c). A capability ticket specifies authorized objects and operations for a particular user. Each user has a number of tickets and may be authorized to loan or give them to others. Because tickets may be dispersed around the system, they present a greater security problem than access control lists. The integrity of the ticket must be protected, and guaranteed (usually by the operating system). In particular, the ticket must be unforgeable. One way to accom- plish this is to have the operating system hold all tickets on behalf of users. These tickets would have to be held in a region of memory inaccessible to users. Another alternative is to include an unforgeable token in the capability. This could be a large random password, or a cryptographic message authentication code. This value is verified by the relevant resource whenever access is requested. This form of capability ticket is appropriate for use in a distributed environment, when the security of its contents cannot be guaranteed.
The convenient and inconvenient aspects of capability tickets are the opposite of those for ACLs. It is easy to determine the set of access rights that a given user has, but more difficult to determine the list of users with specific access rights for a specific resource.

5.   Briefly define the difference between DAC and MAC.


6.   How does RBAC relate to DAC and MAC?
7.   List and define the three classes of subject in an access control system.
8.   What is the difference between an access control list and a capability ticket?
9.   In the NIST RBAC model, what is the difference between SSD and DSD?
10.   What is a protection domain?
11.   UNIX treats file directories in the same fashion as files; that is, both are defined by the same type of data structure, called an inode. As with files, directories include a nine-bit protection string. If care is not taken, this can create access control problems. For example, consider a file with protection mode 644 (octal) contained in a directory with protection mode 730. How might the file be compromised in this case?
12.  what is a session?
13.  give a brief overview of credential management.


Charles Davis II
