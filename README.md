# 🛡️ Active Directory & Windows Server Setup

Documentation of my AD domain, Windows Server 2016 configuration, DNS/DHCP, GPOs, and firewall policies.

---

## 🖥️ Server Info

- OS: Windows Server 2016
- Roles: Active Directory Domain Services, DNS, DHCP
- Hostname: `DC01`
- Domain: `homelab.local`

---

## 🏗️ Setup Steps

### 1. Promote to Domain Controller
- Installed AD DS role
- Promoted to new forest: `homelab.local`

### 2. DNS & DHCP
- Forward lookup zones created
- DHCP scope: `192.168.1.100 - 192.168.1.200`
- DHCP options set (router, DNS)

### 3. Organizational Units (OUs)
- `Users`, `Computers`, `Servers`, `Groups`
- Delegated control on specific OUs

### 4. Group Policy Objects (GPOs)
- Password policy
- Drive mappings
- RDP restrictions
- Software installation (if used)

### 5. Firewall Rules
- Opened only required ports for AD, DNS, DHCP
- Closed RDP to public

---

## 🔧 PowerShell & Scripts

Stored in `/scripts/`  
Example: `create-users.ps1`, `backup-dhcp.ps1`

---

## 🗂️ Notes

- [ ] Backup plan (Windows Server Backup or Veeam)
- [ ] Consider using GPO for hardening
- [ ] Add event log forwarding

---

## 📸 Screenshots

Drop in `/screenshots/` with setup steps, Server Manager, GPO editor, etc.
