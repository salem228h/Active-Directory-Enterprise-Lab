<div align="center">

# 🏢 Active Directory Enterprise Infrastructure Lab

**Enterprise Windows Server 2022 | Active Directory | DNS | DHCP | Group Policy | File Server | Windows 11 Enterprise**

![Windows Server](https://img.shields.io/badge/Windows_Server-2022-0078D6?style=for-the-badge&logo=windows)

![Windows 11](https://img.shields.io/badge/Windows_11-Enterprise-0078D6?style=for-the-badge&logo=windows)

![Active Directory](https://img.shields.io/badge/Active_Directory-Enterprise-blue?style=for-the-badge)

![VirtualBox](https://img.shields.io/badge/VirtualBox-Lab-183A61?style=for-the-badge)

</div>

---

# 📖 Project Overview

This project demonstrates the deployment of a complete Microsoft Active Directory enterprise environment using **Windows Server 2022** and **Windows 11 Enterprise** inside VirtualBox.

The lab follows enterprise best practices for deploying an organization's first Domain Controller, configuring centralized identity management, implementing Group Policy, deploying DHCP and DNS services, configuring secure file sharing, and joining client computers to the domain.

The entire project was built as a hands-on learning environment to simulate tasks commonly performed by IT Support Specialists, Desktop Support Technicians, and Junior System Administrators.

---

# 🎯 Objectives

- Deploy Windows Server 2022

- Configure Static IP Address

- Install Active Directory Domain Services

- Promote Server to Domain Controller

- Configure DNS

- Deploy DHCP

- Create Organizational Units (OU)

- Create Domain Users

- Create Security Groups

- Join Windows 11 to Domain

- Configure Group Policy Objects (GPO)

- Deploy Enterprise File Server

- Configure NTFS Permissions

- Configure Shared Folders

- Test Enterprise Authentication

---

# 🏢 Lab Environment

| Component | Details |
|------------|----------------|
| Hypervisor | VirtualBox |
| Server OS | Windows Server 2022 |
| Client OS | Windows 11 Enterprise |
| Domain | northwind.local |
| Domain Controller | DC01 |

---

# 🌐 Network Configuration

| Device | IP Address |
|------------|----------------|
| DC01 | 192.168.10.10 |
| WS-001 | DHCP |
| DNS Server | 192.168.10.10 |
| DHCP Scope | 192.168.10.100 - 192.168.10.200 |

---

# 🖥️ Enterprise Architecture

```text
                 Internet
                     │
                   NAT
                     │
          +----------------------+
          | Windows Server 2022  |
          |       DC01           |
          | Active Directory     |
          | DNS                  |
          | DHCP                 |
          | File Server          |
          +----------------------+
                     │
          Internal Network
                LABNET
                     │
          +----------------------+
          | Windows 11           |
          | WS-001               |
          | Domain Joined        |
          +----------------------+
```

---

# 📂 Active Directory Structure

```text
northwind.local
│
├── IT
│
├── HR
│
├── Finance
│
├── Sales
│
├── Servers
│
├── Workstations
│
├── Groups
│
└── Service Accounts
```

---

# 👥 Users

| User | Department |
|---------|--------------|
| John Smith | IT |
| Emily Davis | IT |

---

# 🔐 Security Groups

- IT_Admins

- HR_Users

- Finance_Users

- Sales_Users

---

# 📋 Project Phases

## ✅ Phase 1

Windows Server Preparation

- Verify Windows Installation

- Rename Server

- Configure Static IP

- Configure DNS

---

## ✅ Phase 2

Active Directory Installation

- Install AD DS

- Install DNS

---

## ✅ Phase 3

Deploy Domain Controller

- New Forest

- northwind.local

- DNS Configuration

- Promote Domain Controller

---

## ✅ Phase 4

Organizational Units

- Create OU Structure

- Create Users

- Create Security Groups

---

## ✅ Phase 5

Join Windows 11

- Configure Client Network

- Join Domain

- Domain Login

---

## ✅ Phase 6

Group Policy

- Screen Saver

- Control Panel Restriction

- Desktop Policy

- gpupdate

- gpresult

---

## ✅ Phase 7

Enterprise File Server

- Shared Folder

- NTFS Permissions

- Share Permissions

- Domain User Access

---

## ✅ Phase 8

DHCP & DNS

- DHCP Installation

- DHCP Scope

- DNS Configuration

- Client Lease

---

# 💻 Skills Demonstrated

### Windows Administration

- Windows Server 2022

- Windows 11 Enterprise

- Computer Management

- Services

- Event Viewer

---

### Active Directory

- Domain Controller

- Organizational Units

- User Management

- Group Management

- Authentication

---

### Networking

- IPv4

- DNS

- DHCP

- Domain Join

- Name Resolution

---

### Enterprise Administration

- Group Policy

- File Sharing

- NTFS Permissions

- Share Permissions

---

### Security

- Centralized Authentication

- Security Groups

- Access Control

- Least Privilege

---

# 🛠 Technologies Used

- Windows Server 2022

- Windows 11 Enterprise

- Active Directory Domain Services

- DNS Server

- DHCP Server

- Group Policy Management

- VirtualBox

---

# 📁 Repository Structure

```text
Active-Directory-Enterprise-Lab
│
├── README.md
├── LICENSE
├── docs
├── screenshots
├── diagrams
├── scripts
└── assets
```

---

# 📸 Screenshots

The complete deployment process is documented with screenshots for every phase.

- Phase 1

- Phase 2

- Phase 3

- Phase 4

- Phase 5

- Phase 6

- Phase 7

- Phase 8

---

# 📚 Lessons Learned

During this project I gained practical experience in:

- Active Directory deployment

- Enterprise identity management

- DNS configuration

- DHCP deployment

- Group Policy management

- Windows administration

- File Server deployment

- NTFS permissions

- Enterprise troubleshooting

---

# 🔧 Troubleshooting

Common issues addressed during this project:

- DNS resolution problems

- Domain Join failures

- Authentication issues

- Group Policy not applying

- DHCP lease failures

- File Share permission conflicts

---

# 🚀 Future Improvements

- Microsoft Entra ID Integration

- Hybrid Identity

- Microsoft Intune

- Windows Autopilot

- Azure Virtual Machines

- Microsoft 365 Administration

---

# 📜 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Mohammad Salem Hassani**

IT Support | System Administration | Microsoft 365 | Active Directory | Cybersecurity

🇨🇦 Montreal, Quebec, Canada

---

⭐ If you found this project useful, feel free to star the repository.
