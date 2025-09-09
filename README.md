# Wireshark Packet Analysis  

## Overview  
Analyzed captured network traffic to identify normal vs. suspicious activity, with a focus on detecting ARP poisoning.  

## Lab Steps  
1. Captured live traffic on virtual VLAN interface `enp2s0`.  
2. Suspected ARP poisoning → applied ARP display filters.  
3. Detected duplicate use of IP `192.168.0.2`.  
4. Identified responding device MAC address: `00:00:1B:11:22:33`.  
5. Found duplicate MAC address response: `00:00:1B:33:22:11`.  
6. Confirmed ARP poisoning device.  

## Suggested Solution  
- Implement **dynamic ARP inspection (DAI)** on network switches to block spoofed ARP replies.  
- Use **static ARP entries** for critical systems to prevent spoofing.  
- Deploy **intrusion detection systems (IDS)** to alert on suspicious ARP traffic.  

## Key Takeaways  
- Practiced isolating traffic by protocol using Wireshark display filters.  
- Learned how ARP poisoning manipulates IP-to-MAC resolution.  
- Understood that ARP spoofing can allow attackers to intercept or redirect traffic.  
- Reinforced importance of switch-level security (DAI, port security) to mitigate attacks.  

## Screenshots  
