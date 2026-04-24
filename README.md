# Homelab Infrastructure Portfolio

## About This Repository

This repository is the public landing page for my homelab infrastructure projects.

My goal is to document real-world infrastructure work using enterprise-style practices, including:

- Virtualization
- DNS architecture
- Network segmentation
- Firewall policy design
- CI/CD automation
- Monitoring
- Documentation
- Troubleshooting

Sensitive details such as real IP addresses, hostnames, keys, VPN configs, and personal network information are intentionally sanitized.

---

## Current Lab Focus

I am building a production-style homelab environment to strengthen my skills in:

- Systems administration
- Networking
- DevOps
- Linux server management
- Virtualization
- Security-minded infrastructure design

---

## Featured Projects

### Proxmox Virtualization Host

Built a Proxmox VE hypervisor on repurposed enterprise-style hardware.

Focus areas:

- Bare-metal hypervisor install
- Disk cleanup and recovery from failed installs
- Tiered storage design
- SSD boot disk
- NVMe VM storage
- Ubuntu Server VM deployment
- SSH-based administration

Project writeup:

[Proxmox Build Notes](projects/proxmox-build.md)

---

### DNS Infrastructure

Primary and secondary DNS architecture using Pi-hole and Unbound.

Focus areas:

- DNS filtering
- Recursive DNS
- Multi-site DNS planning
- Failover design
- Local DNS records
- Service discovery

Project writeup:

[DNS Stack Notes](projects/dns-stack.md)

---

### Pi-hole Policy Pipeline

Public DNS allow/block policy repository with CI/CD-style workflow.

Focus areas:

- Version-controlled DNS policy
- Group-based allowlists
- GitHub Actions
- Safe deployment planning
- Change tracking

Project writeup:

[Pi-hole Policy Pipeline](projects/pihole-policy-pipeline.md)
https://github.com/Shaw4552/pihole-policy-pipeline

---

### Network Segmentation

Home network redesign using VLANs, firewall policies, and least-privilege access.

Focus areas:

- Infrastructure VLAN
- IoT VLAN
- Kids network
- Guest network
- Work devices
- Firewall rules
- Site-to-site planning

Project writeup:


[Network Design Notes](projects/network-design.md)
https://github.com/Shaw4552/network-segmentation-design

---

## Documentation Philosophy

Each project follows a consistent format:

1. Objective
2. Hardware / software used
3. Design decisions
4. Implementation steps
5. Validation
6. Troubleshooting
7. Lessons learned
8. Next improvements

---

## Security Notice

This repository is intentionally sanitized.

It does not include:

- Real public IP addresses
- VPN keys
- Passwords
- Private hostnames
- Internal secrets
- Full firewall exports
- Sensitive topology details

---

## Long-Term Goal

The goal of this homelab is to build practical, job-relevant experience and demonstrate the ability to design, deploy, document, troubleshoot, and improve real infrastructure systems.
