# Readme - Nmap and Wireshark Task

## Task Summary

In this internship task, i have used **Nmap** tool for scanning and **Wireshark** for packet capturing and analysing. I scanned my **Metasploitable machine** which is running on IP `10.0.2.4` to find which ports are open and which services are running. Then i used Wireshark to observe packets and understand how scanning works behind.

---

## Steps I done

1. **Nmap Already Installed**  
   - I am using Kali Linux, so Nmap already installed by default.

2. **Checked Metasploitable IP**  
   - I logged into Metasploitable VM and used `ip a` to check IP.  
   - It was `10.0.2.4` in my case.

3. **Run TCP SYN Scan**  
   - Command used: `sudo nmap -sS 10.0.2.4`  
   - This command did half-open scan and showed which ports are open.

4. **Noted Down Open Ports**  
   - Found many ports open like 21 (FTP), 22 (SSH), 23 (Telnet), 80 (HTTP), 3306 (MySQL), etc.  
   - I noted these ports for service checking.

5. **Captured Packets Using Wireshark**  
   - Started Wireshark in Kali and ran the scan.  
   - Applied filter: `tcp.flags.syn == 1 && tcp.flags.ack == 0` to see SYN packets.

6. **Checked Packet of Specific Port**  
   - Used filter like `tcp.port == 21` to see FTP-related packets.  
   - Helped me understand which service is being scanned.

7. **Understood Wireshark Color Coding**  
   - Saw different colors for different type of packets (SYN, RST, ACK etc).  
   - Helped me identify communication flow.

8. **Identified Services Running**  
   - I searched on internet what service runs on which port.  
   - Like 22 = SSH, 23 = Telnet, 3306 = MySQL etc.

9. **Found Security Risks**  
   - Found risky ports like Telnet, FTP, SMB etc which are known to be vulnerable.  
   - These should not be open on public network.

10. **Saved Scan Results**  
   - I saved the Nmap scan result using:  
     `sudo nmap -sS 10.0.2.4 -oN scan_result.txt`

---

## Conclusion

By completing this task i learned how to scan a machine using Nmap and how to capture and analyze packets using Wireshark. I learned about common ports and insecure services and how attackers can use this information for attack. Metasploitable was good practice machine for this activity.
---

𝗜𝗮𝗺 𝗱𝗼𝗰𝘂𝗺𝗻𝗲𝗻𝘁𝗲𝗱 𝗲𝘃𝗲𝗿𝘆𝘁𝗵𝗶𝗻𝗴 𝗶𝗻 𝘁𝗵𝗲 𝗧𝗮𝘀𝗸𝟭.𝗽𝗱𝗳

