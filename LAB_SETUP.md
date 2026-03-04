# 🔬 LAB_SETUP.md

## Wireless Security Testing Environment Configuration

This document describes the laboratory environment used to perform the
WPA/WPA2 wireless security assessment.

⚠️ This lab was created for academic and authorized testing purposes
only.

------------------------------------------------------------------------

## 1️⃣ Hardware Configuration

### 💻 Computer System

-   Laptop (Standard CPU -- No GPU acceleration used)
-   Minimum 8GB RAM
-   Virtualization enabled (if using VM)

### 📡 Wireless Adapter

-   Model: Ralink Technology MT7601U
-   Interface Driver: mac80211
-   Monitor Mode: Supported
-   Packet Injection: Supported
-   Connection Type: External USB Adapter

Why External Adapter?\
Most built-in laptop wireless cards do not support monitor mode or
packet injection. An external adapter was used to allow full wireless
penetration testing functionality.

------------------------------------------------------------------------

## 2️⃣ Software Environment

### 🐧 Operating System

-   Kali Linux 2024.2
-   Fully updated before testing

### 🔐 Tools Used

-   Aircrack-ng Suite (v1.7)
-   Airodump-ng
-   Aireplay-ng
-   Wireshark
-   Rockyou.txt wordlist (for dictionary testing)

All tools were used in their default configurations without
modification.

------------------------------------------------------------------------

## 3️⃣ Network Configuration (Test Environment)

The wireless network tested was:

-   Encryption: WPA2-PSK (CCMP)
-   Router: Standard consumer-grade router
-   Channel: Configured manually during testing
-   Environment: Private lab/home setup
-   Authorization: Network owned and fully authorized for testing

No third-party or public networks were targeted.

------------------------------------------------------------------------

## 4️⃣ Test Preparation Steps

Before beginning testing:

1.  System processes interfering with monitor mode were stopped.
2.  Wireless adapter was switched to monitor mode.
3.  Network scan was performed to identify target.
4.  Channel was locked for stable packet capture.
5.  Handshake capture initiated.

------------------------------------------------------------------------

## 5️⃣ Safety and Isolation Measures

To ensure ethical and controlled testing:

-   Testing was performed in a private environment.
-   No corporate or public networks were accessed.
-   No sensitive personal data was intentionally captured.
-   Testing duration was limited to academic demonstration.
-   Results were documented for coursework only.

------------------------------------------------------------------------

## 6️⃣ Limitations of the Lab

-   CPU-only cracking (no GPU acceleration)
-   Single-router environment
-   Limited number of connected devices
-   Dictionary-based attack only (no brute-force full keyspace attack)

Future improvements could include: - GPU-based cracking benchmarks -
WPA3 testing - Enterprise WiFi (802.1X) testing - Advanced wireless
attack simulations

------------------------------------------------------------------------

## 7️⃣ Legal & Ethical Notice

This lab was conducted strictly for educational purposes as part of a
Vulnerability Assessment and Penetration Testing (VAPT) course.

Wireless penetration testing must only be performed on: - Networks you
own - Networks you have written permission to test

Unauthorized access to wireless networks is illegal and unethical.

------------------------------------------------------------------------

## 👩🏽‍💻 Author

Rose Mary Lecha Ngwa Mbenoh\
Cybersecurity Student \| Wireless Security Research \| Ethical Hacking
