# The Pyramid of Pain

<p align="center">
  <img src="https://user-images.githubusercontent.com/90923369/214171416-fa5e76f6-384b-477a-afd5-7d093f79afd9.jpg">
</p>

# What is the Pyramid of Pain?

<p align="center">
  The Pyramid of Pain is an incident response model created in 2013 by David J Bianco. The model depicts a scaling amount of damage that can be inflicted to a threat actor's operations when an indicator of compromise is paired with a quick response from a defensive actor. You can read Davids original blog post on the topic <a href="http://detect-respond.blogspot.com/2013/03/the-pyramid-of-pain.html">here<a/>.
</p>
  
# Level 1: Hash Values
  
  At the base of the pyramid is hash values. When an attacker generates a malicious payload, the payload is assigned a hash value. This hash value is subject to change if just a single bit within the file changes. This means that a malware's source code can easily be modified to change the hash value while retaining the malware's original function. Although malware can be blocked by hash value, Hashes earn their spot at the bottom of the pyramid since there is little work involved for an attacker to bypass a signature check with a new payload that retains the initial function as the original payload.

# Level 2: IP Addresses
  
  Internet protocol addresses sit at Level 2 on the pyramid. Any remote attacker is going to require an IP address to establish CNC communications with an infected host. This means that the IP address can be blocked at the network layer, preventing further communications to the IP address from an infected host. The issue is that there are so many IP addresses that it's trivial for an attacker to simply host their infrastructure under another IP address. This is easily done through services such as the onion router. IP Addresses earn their spot at level 2 since responders could spend weeks blocking IP addresses with little fruit to bear for their labor.
