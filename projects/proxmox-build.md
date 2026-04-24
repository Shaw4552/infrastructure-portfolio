# projects/proxmox-build.md

## Proxmox Virtualization Host Build

### Objective

Deploy a Proxmox VE host to support virtual machines, recovery workflows, desktop testing, and future homelab infrastructure services.

---

## Hardware

- Small-form-factor desktop/server hardware
- 32GB RAM
- SATA SSD used for Proxmox OS
- NVMe SSD used for VM storage
- Wired Ethernet connection

---

## Design Decision

The Proxmox host uses a tiered storage layout:

| Storage | Purpose |
|---|---|
| SATA SSD | Proxmox OS |
| NVMe SSD | VM disks and containers |

This separates the hypervisor from workload storage and improves performance, reliability, and manageability.

---

## Implementation Summary

- Installed Proxmox VE on SATA SSD
- Configured no-subscription repository
- Removed enterprise repository entries
- Updated Proxmox host
- Created NVMe-backed LVM-thin storage
- Created first Ubuntu Server VM
- Enabled SSH-based administration

---

## Troubleshooting Lessons

During installation, I encountered:

- Legacy vs UEFI boot issues
- NVMe boot limitations on older hardware
- Leftover LVM metadata from previous installs
- Repository errors from enterprise Proxmox sources
- VM boot order issues
- SSH login troubleshooting

These were resolved through disk wiping, BIOS review, repository cleanup, and clean VM redeployment.

---

## Current Status

- Proxmox host operational
- Web UI accessible
- SSH access working
- NVMe VM storage configured
- Ubuntu Server VM deployed

---

## Next Steps

- Build Windows recovery VM
- Install Docker on Ubuntu VM
- Add monitoring
- Document backup strategy
- Deploy DNS and infrastructure services