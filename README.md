# Replacing my home ISP router with a virtualized pfSense on Proxmox

<img width="3840" height="2160" alt="labeling" src="https://github.com/user-attachments/assets/06eec926-97cf-4b33-a710-5922bc457667" />

🎥 YouTube videos:
- [Installing proxmox on mini PC and seetting it up for the first time](https://www.youtube.com/watch?v=EQ38efBdF2E)
- [Replacing my home ISP router with pfSense on Proxmox](https://youtu.be/XMvGP2p5xaQ?si=pias_CDBmiZ3KQI5)

---
## 📖 Overview
In this video, I walk through the full process of installing **pfSense** on **Proxmox** step by step. I show how to pass through two PCIe NICs,  
add a virtual NIC for Proxmox access, and explain how the network topology changes at each stage. By the end of the setup, pfSense is managing both physical NICs,  
Proxmox connects to the internet through pfSense, and a dedicated LAN NIC provides DHCP and connectivity for my local network.

---
## 🖼️ Steps / States
**Step 1** – Installing pfSense on Proxmox (Proxmox was installed in my first video)  

**Step 2** – Reviewing my current network situation  
![starting](https://github.com/user-attachments/assets/f5e4963a-3fe7-4a36-b6dd-14c2a75aabfa)  

**Step 3** – Passing my network interfaces directly to pfSense for better performance. From now on, Proxmox has no control over those interfaces.  
![state_after_first_install](https://github.com/user-attachments/assets/71e255d6-3d0d-4272-aae1-844d727b1f96)  

**Step 4** – Configuring pfSense: adding a DHCP server, setting proper IP scopes for LAN clients, and configuring DNS for internet connectivity.  

**Step 5** – Configuring the WAN interface so I can receive a public IP address on this interface, in order to skip NAT on my ISP router (which adds delay).  

**Step 6** – Configuring a virtual interface for Proxmox, so I can access it directly when plugged into the LAN port.  
![final](https://github.com/user-attachments/assets/c67d1cf7-f107-4ddc-96e6-90a736f00c02)  

**Final Result** --> I have full controll over my network and the performance is great, I can not be better.
<img width="729" height="339" alt="speedtest_beforesnort" src="https://github.com/user-attachments/assets/543a7fb4-a7da-4b5c-9738-d2f219401fa2" />


---
All of these steps are explained in more detail in my YouTube video. 🙂
