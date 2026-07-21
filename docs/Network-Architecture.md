# Network Architecture

## Network Design

The lab consists of one Windows Server and one Windows 11 Enterprise client.

```
Internet
    │
   NAT
    │
DC01
192.168.10.10
    │
LABNET
    │
WS-001
DHCP
```

---

## Server

Hostname

DC01

Role

- Domain Controller
- DNS Server
- DHCP Server
- File Server

IP Address

192.168.10.10

---

## Client

Hostname

WS-001

Operating System

Windows 11 Enterprise

Configuration

- Domain Joined
- DHCP Client

---

## Domain

northwind.local

---

## DNS

192.168.10.10

---

## DHCP Scope

192.168.10.100

to

192.168.10.200
