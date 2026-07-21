# Project Ticket Summary

This document contains all work tickets completed during the deployment of the Active Directory Enterprise Infrastructure Lab.

---

# AD-001 – Windows Server Preparation

**Priority:** High

**Status:** ✅ Completed

## Objective

Prepare Windows Server 2022 for Active Directory deployment.

## Tasks

- Install Windows Server 2022
- Rename server to DC01
- Configure Static IP Address
- Configure DNS Server
- Verify network connectivity

## Verification

- hostname
- ipconfig /all
- ping
- nslookup

---

# AD-002 – Install Active Directory Domain Services

**Priority:** High

**Status:** ✅ Completed

## Objective

Deploy Active Directory Domain Services.

## Tasks

- Install AD DS
- Install DNS Server
- Install required features

## Verification

- Server Manager
- AD DS installed successfully

---

# AD-003 – Promote Domain Controller

**Priority:** Critical

**Status:** ✅ Completed

## Objective

Deploy the first Domain Controller.

## Tasks

- Create new forest
- Configure northwind.local
- Configure DSRM password
- Promote server
- Restart server

## Verification

- Domain Controller operational
- DNS operational

---

# AD-004 – Organizational Units & User Management

**Priority:** High

**Status:** ✅ Completed

## Objective

Create the Active Directory structure.

## Tasks

- Create Organizational Units
- Create Domain Users
- Create Security Groups
- Assign users to groups

## Verification

- Active Directory Users and Computers
- Group membership verified

---

# AD-005 – Join Windows 11 Enterprise to Domain

**Priority:** High

**Status:** ✅ Completed

## Objective

Join the client workstation to the Active Directory domain.

## Tasks

- Configure client networking
- Configure DNS
- Join domain
- Restart client
- Login with domain account

## Verification

Commands

hostname

whoami

echo %USERDOMAIN%

gpresult /r

---

# AD-006 – Group Policy Deployment

**Priority:** High

**Status:** ✅ Completed

## Objective

Deploy centralized security policies.

## Tasks

- Create GPO
- Disable Control Panel
- Configure Screen Saver
- Configure Desktop Policy
- Update Group Policy

## Verification

gpupdate /force

gpresult /r

---

# AD-007 – Enterprise File Server

**Priority:** High

**Status:** ✅ Completed

## Objective

Deploy secure enterprise file sharing.

## Tasks

- Create CompanyData folder
- Configure Share Permissions
- Configure NTFS Permissions
- Test domain user access

## Verification

- Domain user successfully accessed shared folder
- Read/Write permissions verified

---

# AD-008 – DHCP & DNS Deployment

**Priority:** High

**Status:** ✅ Completed

## Objective

Deploy centralized IP address management.

## Tasks

- Install DHCP Server
- Configure DHCP Scope
- Configure DNS
- Activate Scope
- Configure Windows 11 as DHCP Client

## Verification

ipconfig /all

ipconfig /renew

nslookup

ping

DHCP lease successfully obtained.

---

# Project Summary

| Ticket | Description | Status |
|---------|-------------|--------|
| AD-001 | Windows Server Preparation | ✅ Completed |
| AD-002 | Install Active Directory Domain Services | ✅ Completed |
| AD-003 | Deploy Domain Controller | ✅ Completed |
| AD-004 | Organizational Units & User Management | ✅ Completed |
| AD-005 | Join Windows 11 to Domain | ✅ Completed |
| AD-006 | Group Policy Deployment | ✅ Completed |
| AD-007 | Enterprise File Server | ✅ Completed |
| AD-008 | DHCP & DNS Deployment | ✅ Completed |

---

## Overall Result

The Active Directory Enterprise Infrastructure Lab was successfully deployed.

### Services Implemented

- Windows Server 2022
- Active Directory Domain Services
- DNS
- DHCP
- Organizational Units
- Domain Users
- Security Groups
- Windows 11 Enterprise
- Domain Join
- Group Policy
- Enterprise File Server
- NTFS Permissions

The environment is fully operational and demonstrates practical enterprise system administration skills using Microsoft technologies.
