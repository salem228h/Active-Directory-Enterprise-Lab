# Troubleshooting Guide

## Domain Join Failed

Cause

Incorrect DNS configuration.

Resolution

Verify the DNS server points to the Domain Controller.

---

## Group Policy Not Applying

Command

gpupdate /force

gpresult /r

---

## DNS Resolution Failed

Command

nslookup northwind.local

---

## DHCP Not Leasing

Check:

- DHCP Service
- Active Scope
- Client Configuration

---

## Shared Folder Access Denied

Verify:

- Share Permissions
- NTFS Permissions
- Group Membership
