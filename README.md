# Wi-Fi Traffic Analysis Project

Welcome to the **Wi-Fi Password cracking project**! This repository documents a cybersecurity project where we analyze network traffic from a Wi-Fi network to understand device communications, protocols, and potential vulnerabilities.

---

## **Overview**
This project demonstrates how to:

- Capture Wi-Fi traffic using an Alfa AWUS1900 adapter in monitor mode.
- Perform a deauthentication attack to capture device handshake traffic (ethical and on a self-owned network).
- Analyze decrypted Wi-Fi traffic in Wireshark to observe:
  - Device behavior and protocols.
  - Service discovery (MDNS).
  - DHCP, ARP, ICMPv6, and multicast traffic.

The focus is on learning ethical hacking techniques and understanding network protocols without delving into password cracking or unauthorized access.

---

## **Features of the Project**

1. **Traffic Capture**
   - Wi-Fi traffic captured using the Alfa AWUS1900 adapter in monitor mode.
   - Targeted capture of EAPOL handshake packets and device-specific traffic.

2. **Traffic Analysis**
   - Observing protocols like MDNS, ARP, DHCP, ICMPv6, and IGMPv3.
   - Identifying device-specific traffic patterns and hostnames.
   - Learning about multicast groups and service discovery mechanisms.

3. **Ethical Approach**
   - The project focuses solely on ethical hacking and network analysis.
   - Password cracking or unauthorized access steps were not included in the documentation or video.

4. **Video Walkthrough**
   - The repository includes a video demonstration of the traffic analysis process.
   - The video shows practical use of AWUS1900 to analyze live traffic from wifi networks and what a potential attacker might look for.

---

## **Technical Setup**
### Tools and Technologies Used:
- **Kali Linux**
- **Wireshark** for traffic analysis
- **Aircrack-ng Suite** for network capture
- **Alfa AWUS1900** Wi-Fi adapter in monitor mode

### Key Steps:
1. **Set Up Monitor Mode:**
   - Placed Wi-Fi adapter in monitor mode to capture raw packets.
   ```bash
   sudo airmon-ng start wlan0
   ```

2. **Deauthentication Attack:**
   - Conducted a deauthentication attack to force a device to reconnect and capture handshake packets (performed ethically on a self-owned network).
   ```bash
   sudo aireplay-ng --deauth 10 -a <Router_BSSID> --channel <CH> wlan0
   ```

3. **Traffic Analysis in Wireshark:**
   - Filtered traffic using:
     - Device-specific MAC address:
       ```plaintext
       wlan.addr == <Phone_MAC>
       ```
     - Protocol-specific filters like DNS, ARP, and ICMPv6.

---

## **What You Can Learn**
- How network protocols like ARP, DHCP, and MDNS work in real-world scenarios.
- Methods attackers might use to identify devices and gather metadata.
- Practical techniques to monitor and secure your own network.

---

## **What’s Included in the Repository**
1. **Screenshots:**
   - Key screenshots of Wireshark traffic analysis.

     ![PhoneConnectingToPCkde](https://github.com/user-attachments/assets/06594e2a-3200-4504-ad51-14b8aca2eec2)


2. **Video Demonstration:**
   - A comprehensive video walkthrough of the traffic analysis process.
   - Focus on understanding protocols and identifying device behavior.


https://github.com/user-attachments/assets/b44f2333-990e-41b6-aa08-310433cf1325


---

## **Ethical Considerations**
This project was conducted ethically on a self-owned network with full permissions. The aim is to educate and promote better network security practices, not to facilitate malicious activities.

---

## **Acknowledgments**
This project was inspired by the desire to learn ethical hacking and improve network security knowledge.

---
