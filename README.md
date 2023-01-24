# The Pyramid of Pain

<p align="center">
  <img src="https://user-images.githubusercontent.com/90923369/214171416-fa5e76f6-384b-477a-afd5-7d093f79afd9.jpg">
</p>

# What is the Pyramid of Pain?

<p align="center">
  The Pyramid of Pain is an incident response model created in 2013 by David J Bianco. The model depicts a scaling amount of damage that can be inflicted to a threat actor's operations when an indicator of compromise class from the pyramid is paired with a quick detection and response from a defensive actor. You can read Davids original blog post on the topic <a href="http://detect-respond.blogspot.com/2013/03/the-pyramid-of-pain.html">here<a/>.
</p>
  
# Level 1: Hash Values
  
  At the base of the pyramid is hash values. When an attacker generates a malicious payload, the payload is assigned a hash value. This hash value is subject to change if just a single bit within the file changes. This means that a malware's source code can easily be modified to change the hash value while retaining the malware's original function. Although malware can be blocked by hash value, Hashes earn their spot at the bottom of the pyramid since there is little work involved for an attacker to bypass a signature check with a new payload that retains the initial function as the original payload.

# Level 2: IP Addresses
  
  Internet protocol addresses sit at Level 2 on the pyramid. Any remote attacker is going to require an IP address to establish CNC communications with an infected host. This means that the IP address can be blocked at the network layer, preventing further communications to the IP address from an infected host. The issue is that there are so many IP addresses that it's trivial for an attacker to simply host their infrastructure under another IP address. This is easily done through services such as the onion router. IP Addresses earn their spot at level 2 since responders could spend weeks blocking IP addresses with little fruit to bear for their labor.

# Level 3: Domains

Often, an attacker will utilize a domain for resolving IP addresses within their payloads call back. This allows the attacker to use any number of IP addresses and retain communications to infected hosts from their CNC infrastructure. When a domain has been blocked at layer 7, an attacker will need to purchase, register, host and modify records on the domain. The domain will then require up to 48 hours time to propagate across name servers on the internet before it's completely ready for abuse. Domains are relatively easy to acquire or rename, however they earn their spot at Level 3 since the adversary must put some time and effort into acquiring a new domain that has not placed into a deny-list, sinkhole or other prevention mechanism.

# Level 4: Network / Host Artifacts

Artifacts are pieces of data left behind by the presence of malware. A host artifact could be a registry key change or a file that is being written to by the malicious process. A network artifact could be a unique user agent string, URI patterns, SMTP mailer values or other data that traverses the network which is unique to the malware producing the traffic. Ideally, a responder will block communications on the network based on the presence of known artifacts such as a specific user agent in a web request. Artifacts earn their spot at level 4 since detection and response will often result in the attacker expending their time performing reconfiguration of the malware while investigating how and why the malware was detected.

# Level 5: Tools
  
Tools are defined as the software that an attacker uses to establish initial access, escalate privileges and act on objectives. Typically, they are packed in with the attacker after initial access is gained, rather than living off the land. When a response team has developed enough detection methods for the attacker's tooling, the attacker will be forced to acquire new tooling, which takes valuable time away from the attacker's objectives since their time is invested in the acquisition of and training with the new tooling. Tools earn their spot at level 5 since their prompt detection forces the attacker back to the drawing board for a greater period of time.

# Level 6: Tactics, Techniques and Procedures

TTP refers to the Tactics, Techniques and Procedures used by adversaries to accomplish their mission, from reconnaissance to action on objectives. TTP does not refer to specific tooling, but rather the methods used by the tooling to accomplish the adversaries goals, as outlined in the <a href="https://attack.mitre.org">MITRE ATT&CK Matrix</a>. For example, a man in the middle attack is a technique that many software pieces are capable of such as ettercap and bettercap however they both utilize the same technique (MiTM) to capture data traversing the network from targeted hosts. Tactics, Techniques and Procedures earn their spot at Level 6 since detection and response renders the TTP's useless, regardless of the software or configuration that the adversary is using. Depending on the adversaries motivations, the adversary will invest a great deal of time in researching and developing new TTP's to accomplish their goals or find a new target that remains vulnerable to their current TTP's.

# Conclusion
  
The Pyramid of Pain represents a scalable model in which the "pain" for either the defender or the attacker is based on the indicator of compromise that the defenders focus their attention on. If defenders aim for the lower tiers of the pyramid, the attacker will have an easier time bypassing the defenses put in place, meaning the defender's time is wasted. When defenders aim for the higher levels of the pyramid, they are able to slow down or completely demotivate an attacker since the attacker will now spend more time attempting to attack a single target rather than successfully attacking three targets in the amount of time that the single attempt takes. This outcome ultimately depends on the attacker's motivation, as a financially motivated attacker will likely take the stick and move approach, whereas the hacktivist will commit to attacking the single target who has violated their ideology.
  
# Further Reading
<a href="http://detect-respond.blogspot.com/2013/03/the-pyramid-of-pain.html">Davids original blog post on the Pyramid of Pain</a>   
  
<a href="https://cyware.com/educational-guides/cyber-threat-intelligence/the-concept-of-pyramid-of-pain-f358">CyWare: The Concept of Pyramid of Pain</a>  
  
<a href="https://www.attackiq.com/glossary/pyramid-of-pain/">AttackIQ: What is the Pyramid of Pain?</a>  
