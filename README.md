
Yeh repository mere Cybersecurity aur Ethical Hacking lab environment ke setup ko document karti hai. Is lab ko maine apne laptop par configure kiya hai taake main aage aane wale penetration testing aur network security ke modules practice kar sakoon.

 Lab Architecture & Specifications

Lab ko VirtualBox ke zariye set up kiya gaya hai taake ek secure aur isolated environment banaya ja sake.

*   **Host OS:** Windows 10 (HP EliteBook)
*   **Hypervisor:** Oracle VM VirtualBox
*   **Attacker Machine:** Kali Linux (Pre-built VirtualBox Image)
*   **Network Subnet:** `10.0.0.0/24`
*   **Network Type:** NAT Network
*   **Kali Linux IP:** `10.0.0.2/24`

Setup Steps (Phase 1)

Maine apne lab ko set up karne ke liye yeh steps follow kiye:

1.  **VirtualBox Installation:** VirtualBox ki latest version install ki.
2.  **NAT Network Creation:** VirtualBox ki preferences mein jaakar ek naya NAT Network banaya jiska IPv4 Prefix `10.0.0.0/24` set kiya.
3.  **Kali Linux Import:** Kali Linux ki official website se pre-built VM download ki, extract ki, aur VirtualBox mein import kiya.
4.  **VM Settings Configuration:** 
    *   Network Adapter ko **NAT Network** se connect kiya.
    *   **Shared Folders** enable kiye (Host ka `Downloads` folder share kiya taake file transfer aasan ho).
    *   **Clipboard** aur **Drag'n'Drop** ko *Bidirectional* set kiya.
5.  **IP Configuration:** Kali Linux ke terminal mein `nmcli` commands ka istemal karke apni machine ko static IP `10.0.0.2/24` assign kiya.
6.  **Verification:** `ping` aur `ip a` commands chala kar confirm kiya ke internet aur network connectivity bilkul theek chal rahi hai.
7.  **Snapshot:** Poora setup hone ke baad VirtualBox mein ek snapshot (naam: *Lab Setup Complete*) liya taake future mein kharab hone par wapas isi state par aaya ja sake.

 Verification Commands

Lab ke theek se chalne ko confirm karne ke liye maine yeh commands run ki hain:
*   `ip a` -> IP Address verify karne ke liye (`10.0.0.2`)
*   `ping -c 4 google.com` -> Internet connectivity test karne ke liye
*   `df -h` -> Disk space check karne ke liye
*   `uptime` -> System ki running time check karne ke liye
##  Next Steps (Phase 2)
*   Windows 10/11 aur Android VM ko isi NAT Network mein add karna.
*   Alag alag machines ko aapas mein ping karke connectivity test karna.
