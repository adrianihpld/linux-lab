# Linux Lab

An overview of my homelab, which I'm building to showcase the following:

- Linux system administration (RHEL-based)
- Configuration management with Ansible
- Virtualization with VMware Workstation / Proxmox
- Infrastructure as Code (IaC)
- Networking, DNS, and system monitoring
- Kubernetes container orchestration

## Lab Overview

This lab is deployed across two physical machines and two labs (homelab & worklab):

### Machine 1: 6-core, 64 GB RAM

- ansible-control: Infrastructure as Code with Ansible (provisions all VMs)
- podman-dev: Podman container testing & development
- k8s-worker-1: Kubernetes worker node

### Machine 2: 8-core, 32 GB RAM

- k8s-master: Kubernetes control plane
- k8s-worker-2: Kubernetes worker node
- monitoring: Prometheus & Grafana (cluster metrics)

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
- systemd
- Nextcloud, Apache, Packer

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

