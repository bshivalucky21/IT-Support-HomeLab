
# Lab Architecture

This lab simulates a small business environment with:
- Domain Controller (AD DS + DNS)
- Windows client joined to the domain
- File shares controlled by NTFS + Share permissions + ABE
- Ubuntu server hosting osTicket to manage incidents and requests

See the diagram: `lab-diagram.png`



flowchart LR
  subgraph VMware["VMware Virtual Network (Host-Only / NAT)"]
    W11["W11-CLIENT\nWindows 11\nDomain Joined"] -->|HTTP (Open Ticket)| OST["Ubuntu Server\nApache + PHP + osTicket"]
    W11 -->|LDAP/Kerberos/DNS| DC["DC01\nWindows Server 2022\nAD DS + DNS"]
    W11 -->|SMB (S: Drive)| FS["DC01 (File Server Role)\nShares + NTFS + ABE + FSRM"]
  end

  DC --- FS

  style DC fill:#f5f5f5,stroke:#333,stroke-width:1px
  style OST fill:#f5f5f5,stroke:#333,stroke-width:1px
  style W11 fill:#f5f5f5,stroke:#333,stroke-width:1px
  style FS fill:#f5f5f5,stroke:#333,stroke-width:1px
