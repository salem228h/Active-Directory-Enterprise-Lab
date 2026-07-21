<div align="center">

# 🏢 Active Directory Enterprise Infrastructure Lab

**A complete Microsoft enterprise environment built from scratch in VirtualBox**

![Windows Server](https://img.shields.io/badge/Windows_Server-2022-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![Windows 11](https://img.shields.io/badge/Windows_11-Enterprise-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![Active Directory](https://img.shields.io/badge/Active_Directory-Enterprise-5C2D91?style=for-the-badge&logo=microsoft&logoColor=white)
![VirtualBox](https://img.shields.io/badge/VirtualBox-Lab-183A61?style=for-the-badge&logo=virtualbox&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-success?style=for-the-badge)

</div>

---

## 📌 Overview

This project demonstrates a **full Microsoft Active Directory enterprise deployment** using Windows Server 2022 and Windows 11 Enterprise inside VirtualBox.

Built to simulate the real-world tasks performed by IT Support Specialists, Desktop Support Technicians, and Junior System Administrators — covering identity management, DNS/DHCP, Group Policy, file services, and NTFS permissions from end to end.

---

## 📊 At a Glance

| | |
|---|---|
| 🖥️ **VMs** | 2 (DC01 + WS-001) |
| 🏗️ **Phases** | 8 |
| 🗂️ **OUs** | 8 |
| 📋 **GPOs** | 6+ |
| 🌐 **Domain** | northwind.local |
| 🔧 **Hypervisor** | VirtualBox |

---

## 🌐 Network Architecture

```
                      Internet
                          │
                        NAT
                          │
             ┌────────────────────────┐
             │   Windows Server 2022  │
             │         DC01           │
             │   192.168.10.10        │
             │                        │
             │  ● Active Directory    │
             │  ● DNS Server          │
             │  ● DHCP Server         │
             │  ● File Server         │
             └────────────────────────┘
                          │
                   LABNET (Internal)
                          │
             ┌────────────────────────┐
             │    Windows 11 Ent.     │
             │        WS-001          │
             │   DHCP (192.168.10.x)  │
             │   Domain Joined        │
             └────────────────────────┘
```

| Device | IP Address | Role |
|--------|-----------|------|
| DC01 | 192.168.10.10 | Domain Controller / DNS / DHCP / File Server |
| WS-001 | DHCP (.100–.200) | Domain-joined workstation |

---

## 🗂️ Active Directory Structure

```
northwind.local
│
├── 👥 IT
├── 👥 HR
├── 👥 Finance
├── 👥 Sales
├── 🖥️ Servers
├── 💻 Workstations
├── 🔐 Groups
└── ⚙️ Service Accounts
```

### Users & Groups

| User | Department |
|------|-----------|
| John Smith | IT |
| Emily Davis | IT |

**Security Groups:** `IT_Admins` · `HR_Users` · `Finance_Users` · `Sales_Users`

---

## ✅ Deployment Phases

| Phase | Name | Key Tasks |
|-------|------|-----------|
| 1 | **Server Preparation** | Rename server · Static IP · DNS baseline |
| 2 | **AD DS Installation** | Install AD DS and DNS roles |
| 3 | **Domain Controller Promotion** | New forest · northwind.local · DNS config |
| 4 | **OU, Users & Groups** | 8 OUs · domain users · security groups |
| 5 | **Windows 11 Domain Join** | Client network config · join · login test |
| 6 | **Group Policy Objects** | Screen saver · control panel restriction · desktop policy · gpupdate/gpresult |
| 7 | **Enterprise File Server** | Shared folders · NTFS permissions · share permissions · access test |
| 8 | **DHCP & DNS** | DHCP scope · DNS zones · client lease verification |

---

## 💻 Skills Demonstrated

### Windows Administration
`Windows Server 2022` `Windows 11 Enterprise` `Computer Management` `Event Viewer` `Services`

### Active Directory
`Domain Controller` `Organizational Units` `User Management` `Group Management` `Authentication`

### Networking
`IPv4` `DNS` `DHCP` `Domain Join` `Name Resolution`

### Enterprise Administration
`Group Policy` `File Sharing` `NTFS Permissions` `Share Permissions`

### Security
`Centralized Authentication` `Security Groups` `Access Control` `Least Privilege`

---

## 🛠️ Technologies Used

| Category | Technology |
|----------|-----------|
| Server OS | Windows Server 2022 Standard |
| Client OS | Windows 11 Enterprise |
| Directory | Active Directory Domain Services |
| Network Services | DNS Server · DHCP Server |
| Policy | Group Policy Management Console |
| Hypervisor | Oracle VirtualBox |

---

## 📁 Repository Structure

```
Active-Directory-Enterprise-Lab/
│
├── README.md
├── LICENSE
├── docs/
│   └── deployment-guide.md
├── screenshots/
│   ├── phase-1/
│   ├── phase-2/
│   └── ... (phase 3–8)
├── diagrams/
│   └── network-topology.png
├── scripts/
│   └── ad-setup.ps1
└── assets/
```

---

## 📚 Lessons Learned

- How Active Directory centralizes identity across an enterprise
- Why DNS is the backbone of every AD deployment — break DNS, break the domain
- How Group Policy propagates security settings at scale without touching each machine
- The difference between NTFS permissions and Share permissions — and why both matter
- DHCP lease lifecycle and how clients resolve names via the DC

---

## 🔧 Common Issues & Fixes

| Issue | Root Cause | Fix |
|-------|-----------|-----|
| DNS resolution failure | DC IP not set as DNS on client | Point client DNS to 192.168.10.10 |
| Domain join fails | Network adapter misconfigured | Switch to Internal Network in VirtualBox |
| GPO not applying | gpupdate not run after change | Run `gpupdate /force` on client |
| DHCP lease not issued | Scope not activated | Authorize and activate scope in DHCP console |
| File share access denied | NTFS vs Share permission conflict | Grant permissions at both levels |

---

## 🚀 Future Improvements

- [ ] Microsoft Entra ID (Azure AD) integration
- [ ] Hybrid identity with Entra Connect
- [ ] Microsoft Intune — MDM policy management
- [ ] Windows Autopilot deployment
- [ ] Azure Virtual Machines
- [ ] Microsoft 365 administration

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 👨‍💻 Author

**Mohammad Salem Hassani**
IT Support | System Administration | Microsoft 365 | Active Directory | Cybersecurity
🇨🇦 Montreal, Quebec, Canada

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat&logo=linkedin)](https://linkedin.com/in/mohammad-salem-hassani)

---

<div align="center">
⭐ If this project helped you, consider starring the repository
</div>
