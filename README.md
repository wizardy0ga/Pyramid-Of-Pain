# The Pyramid of Pain

<p align="center">
  <img src="https://user-images.githubusercontent.com/90923369/214171416-fa5e76f6-384b-477a-afd5-7d093f79afd9.jpg">
</p>

# What is the Pyramid of Pain?

<p align="center">
  The Pyramid of Pain is an incedent response model created in 2013 by David J Bianco. The model depicts a scaling amount of damage that can be inflicted to a threat actors operations when an indicator of compromise is paired with a quick response from a defensive actor. You can read Davids original blog post on the topic <a href="http://detect-respond.blogspot.com/2013/03/the-pyramid-of-pain.html">here<a/>.
</p>
  
# Level 1: Hash Values
  
  At the base of the pyramid is hash values. When an attacker generates a malicious payload, the payload is assigned a hash value. This hash value is subject to change if just a single byte within the file changes. This means that a malwares source code can easily be modified to change the hash value while retaining the malwares original function. Although malware can be blocked by hash value, Hashes earn their spot at the bottom of the pyramid since there is little work involved for an attacker to bypass a signature check with a new payload that retains the initial function as the original payload.
