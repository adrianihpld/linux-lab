# Linux Lab

This is my personal Linux homelab built for learning and showcasing skills in:

- Linux system administration (RHEL-based)
- Configuration management with Ansible
- Virtualization with VMware Workstation / Proxmox
- Infrastructure as Code (IaC)
- Networking, DNS, and system monitoring
- Kubernetes container orchestration

## Lab Overview

This lab is deployed across two physical machines:

### Machine 1: 6-core, 64 GB RAM

- Ansible control node
- DNS server
- Logging & monitoring stack
- Git repository management

### Machine 2: 8-core, 32 GB RAM

- Podman container host
- Kubernetes worker node (future)
- Web server & test workloads

## Directory Structure

linux-lab/
├── ansible/
│ ├── inventory/
│ │ ├── hosts # Safe sample inventory file
│ │ └── hosts.local # Real IPs (excluded via .gitignore)
│ └── playbooks/ # Ansible playbooks go here
├── .gitignore # Prevents sensitive files from being committed
└── README.md # Project documentation

## Technologies Used

- Red Hat Enterprise Linux 9
- Ansible
- Podman / Docker
- firewalld / SELinux
- tmux / vim / iTerm2
- Git + GitHub

## Later Versions Will Include
systemd
Nextcloud, Apache, Packer

## Goals

- Practice real-world Linux administration
- Automate VM setup and service configuration using Ansible
- Deploy and manage containers with Podman
- Prepare for RHCSA / RHCE / SRE roles
- Build a reproducible, documentable homelab project

## Security and GitHub Notes

- All sensitive files (e.g., real IPs) are kept in `hosts.local` and ignored by Git.
- `hosts` contains sanitized examples safe for GitHub.
- All infrastructure code and playbooks are tracked with Git for version control.

