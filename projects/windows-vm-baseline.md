# Windows 10 VM Baseline Build

## Objective

Deploy and configure a Windows 10 virtual machine on Proxmox to serve as a reusable baseline for recovery, testing, and administrative workloads.

---

## Environment

- Platform: Proxmox VE
- VM Name: win10-recovery
- CPU: 4 cores
- RAM: 8GB
- Disk: 120GB (VirtIO SCSI)
- BIOS: UEFI (OVMF)
- Storage: NVMe-backed LVM-thin

---

## Implementation Summary

### 1. VM Creation
- Created VM in Proxmox
- Configured VirtIO SCSI controller
- Enabled UEFI boot
- Attached Windows 10 ISO + VirtIO driver ISO

---

### 2. Windows Installation
- Installed Windows 10 Pro (x64)
- Completed initial setup with local account
- Configured basic system settings

---

### 3. Driver Integration (Critical)
- Loaded VirtIO storage drivers during install
- Installed:
  - viostor (storage)
  - vioscsi (SCSI controller)
- Resolved disk detection issue

---

### 4. Guest Optimization
- Installed VirtIO guest tools
- Enabled:
  - Network drivers
  - Storage performance optimization
  - Improved VM responsiveness

---

### 5. Networking
- DHCP IP assigned successfully
- Verified internet connectivity
- Configured network as Private
- Enabled network discovery

---

### 6. Remote Access
- Enabled Remote Desktop (RDP)
- Verified local user access
- Prepared for remote administration

---

## Current Status

- Windows installation complete
- VirtIO drivers installed
- Network connectivity confirmed
- System currently undergoing Windows Updates
- OS version requires upgrade to supported release (22H2)

---

## Next Steps

- Complete Windows Updates to latest version
- Verify system fully patched
- Install baseline tools:
  - 7-Zip
  - Notepad++
  - VS Code (optional)
- Rename system using naming convention:
  - win10-recovery-01
- Create Proxmox snapshot:
  - win10-baseline-v1

---

## Lessons Learned

- VirtIO drivers are required for disk visibility in Proxmox
- Multiple driver versions exist; correct OS version must be selected
- Older Windows ISOs significantly increase update time
- Proper snapshot timing is critical (post-update only)

---

## Status

🟡 In Progress – Awaiting completion of Windows Updates before baseline snapshot