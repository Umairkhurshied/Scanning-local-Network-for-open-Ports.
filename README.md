# Scanning-local-Network-for-open-Ports.
Discovering open ports on a device in the local network to understand network exposure.
# Local Network Port Scanning with Nmap

This project demonstrates how I scanned my local network to identify active devices and open ports using **Nmap**, a powerful network scanning tool. The goal was to understand basic network reconnaissance techniques and identify potential security risks from exposed services.

## 🔧 Steps Performed

1. **Installed Nmap**  
   Installed Nmap on my system using the official documentation or package manager (`apt`, `brew`, etc.).

2. **Found Local IP Range**  
   Determined my local IP address and subnet (e.g., `192.168.1.0/24`) using commands like `ip a`, `ifconfig`, or `ipconfig`.

3. **Performed SYN Scan**  
   Ran a TCP SYN scan on the entire subnet using the following command:
              nmap -sS 192.168.1.0/24
   4. **Analyzed Scan Output**  
- Noted all live hosts and their open ports.
- Researched common services associated with those ports (e.g., port 22 = SSH, port 80 = HTTP).

5. **Identified Potential Risks**  
- Evaluated which services might pose a security risk if left exposed.
- Considered how these ports could be exploited in an insecure network.

6. **Saved Scan Results**  
- Saved the output to a text file for documentation and later reference:
              nmap -sS 192.168.1.0/24 -oN scan_result.txt
