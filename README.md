# Wireless Network Security Assessment  
## WPA/WPA2-PSK Password Cracking & Traffic Analysis (Lab Environment)

## Project Overview

This project documents a full Wireless Network Vulnerability Assessment and Penetration Testing (VAPT) exercise conducted in a controlled lab environment.

The objective was to evaluate the security of a WPA2-PSK protected wireless network by:

- Capturing a WPA handshake
- Performing a dictionary attack
- Analyzing network traffic using Wireshark
- Assessing overall security risks
- Providing remediation recommendations

⚠️ All testing was performed on a personally owned lab network for academic purposes.

---

## 🎯 Executive Summary

The WPA2-PSK password was successfully cracked using a dictionary attack.

### Key Results:
-  WPA2 password successfully recovered
-  Time taken: 11 hours 48 minutes
-  Passwords tested: 10,303,727
-  Packets captured: 312,787
-  Overall Risk Level: CRITICAL

The password was extremely weak and appeared early in a common password list.

---

## Tools & Technologies Used

- Kali Linux 2024.2
- Aircrack-ng Suite (v1.7)
- Airodump-ng
- Aireplay-ng
- Wireshark
- Rockyou.txt wordlist (14M+ passwords)
- Ralink MT7601U (Monitor mode + Packet Injection supported)

---

## 🧪 Lab Environment

- WPA2-CCMP (PSK) secured WiFi network
- External USB WiFi adapter in monitor mode
- Dictionary attack using rockyou.txt
- Traffic analysis using Wireshark

---

## 🔎 Methodology

### 1️⃣ Monitor Mode Configuration
Enabled monitor mode to capture all wireless packets.

Outcome:
- Wireless interface successfully switched to monitor mode.

---

### 2️⃣ Network Discovery
Scanned for nearby networks and identified target.

Observed:
- Multiple WPA2 and WPA3 networks
- Strong signal strength
- Active connected clients

---

### 3️⃣ WPA Handshake Capture

Steps:
- Targeted specific channel
- Captured packets
- Performed deauthentication to force client reconnection
- Successfully captured WPA 4-way handshake

Results:
- Handshake captured in 3 minutes
- 7,478 packets recorded
- Capture file generated

---

### 4️⃣ Dictionary Attack (Password Cracking)

Used Aircrack-ng with rockyou.txt wordlist.

Results:
- Password recovered successfully
- 10,303,727 keys tested
- Speed: 242.33 keys/second (CPU-based)
- Total cracking time: 11h 48m

📌 Demonstrates vulnerability of weak passwords even under WPA2 encryption.

---

### 5️⃣ Traffic Analysis (Wireshark)

Total packets analyzed: 312,787

Observed:

- 802.11 Management frames
- Beacon frames
- Authentication frames
- QoS Data packets
- Broadcast traffic
- Multiple device MAC addresses exposed
- Traffic patterns between clients

Security Insight:
Even when encrypted, metadata exposure reveals network structure and device activity.

---

## 🚨 Findings

### 🔴 Finding 1: Extremely Weak Password (CRITICAL)

- Password cracked within 12 hours
- Found early in common password list
- Vulnerable to basic dictionary attacks

Impact:
- Unauthorized network access
- Data interception
- Device compromise risk

---

### Finding 2: Deauthentication Attack Possible (HIGH)

- Network vulnerable to disconnect attacks
- Used to force handshake capture

Impact:
- Service disruption
- Easier credential capture

Mitigation:
- Enable Protected Management Frames (802.11w)

---

###  Finding 3: Information Exposure (MEDIUM)

Visible Information:
- SSID broadcasting
- Router MAC address
- Client MAC addresses
- Device manufacturers
- Channel and encryption type

Impact:
- Network mapping
- Targeted attack planning

---

##  Technical Metrics

- Handshake capture time: 3 minutes
- Total cracking duration: ~12 hours
- Keys tested: 10.3M
- Packet count analyzed: 312,787
- Hardware: Standard CPU (No GPU acceleration)

With GPU acceleration, crack time could drop from hours to minutes.

---

## Security Recommendations

1. Use minimum 20-character random password
2. Avoid dictionary words
3. Enable WPA3 if supported
4. Enable Protected Management Frames
5. Disable WPS
6. Create separate guest network
7. Enable router firewall
8. Regularly update firmware
9. Monitor connected devices monthly

---

## Skills Demonstrated

- Wireless penetration testing
- WPA2 handshake capture
- Deauthentication attack simulation
- Dictionary attack methodology
- Packet-level traffic analysis
- Risk assessment & reporting
- Security recommendations development
- Technical documentation

---

## Ethical Disclaimer

This project was conducted strictly for academic purposes as part of a VAPT course. All testing was performed in a controlled lab environment on authorized systems.

Unauthorized wireless network testing is illegal and unethical.

---

## Author

Rose Mary Lecha Ngwa Mbenoh  
Cybersecurity | Network Security | Ethical Hacking  
