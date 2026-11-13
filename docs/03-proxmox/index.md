# Proxmox VE

Proxmox Virtual Environment (VE) is a powerful, open-source hypervisor platform that lets you run and manage multiple virtual machines (VMs) and containers on a single physical server. It's based on Debian Linux, with a web-based interface, support for ZFS, LXC containers, KVM virtualization, backups, snapshots, clustering, and more.

Proxmox is ideal for homelabs and media servers because it:

- Provides full control and visibility over your hardware and services.
- Lets you separate concerns (e.g., media streaming, storage, DNS) into isolated VMs or containers.
- Is lightweight and robust for long-running infrastructure.

## Installation

Refer to [Installing Proxmox VE](https://pve.proxmox.com/pve-docs/chapter-pve-installation.html).

This section is to be updated.

## Using Proxmox VE

Proxmox VE provides a powerful, browser-based interface to manage virtual machines, containers, storage, networking, and backups.

### Web Interface

Access the web UI at: `https://your-server-ip:8006`

Login with the `root` user and your Debian system password.

From here you can:

- Create and manage **virtual machines (VMs)** and **containers (LXC)**
- Monitor CPU, memory, disk, and network usage
- Configure **storage** for VM disks, containers, and backups
- Manage **backups**, snapshots, and restore points
- Set up **network bridges** and VLANs
- Perform system updates and manage user access

### VMs vs Containers

Proxmox supports two types of virtualization:

| Feature            | Virtual Machine (KVM)             | Container (LXC)                |
|--------------------|----------------------------------|-------------------------------|
| Isolation          | Full (runs its own kernel)       | Partial (shares host kernel)  |
| OS Compatibility   | Any OS (Linux, Windows, etc.)    | Linux-only                    |
| Resource Usage     | Higher                           | Lower                         |
| Use Case           | Complex apps, legacy software    | Lightweight services (e.g., Jellyfin, Pi-hole) |

Use containers where possible for performance and simplicity. Use VMs when you need full OS-level isolation or non-Linux systems.

### Storage Management

Proxmox supports various storage types:

- **Local storage** (e.g. SSD, HDD)
- **ZFS** (ideal for snapshots, replication, and integrity checking)
- **Network shares** (NFS, SMB/CIFS, iSCSI)

You can create storage pools for:

- VM and container disks
- ISO images and templates
- Backups and snapshots

### Resource Monitoring

The web interface includes dashboards and graphs for:

- CPU and RAM usage
- Disk I/O and throughput
- Network traffic
- Node health and load

You can also enable email alerts or integrate with external monitoring tools like **Netdata**, **Grafana**, or **Prometheus**.

## Maintenance

How do you keep things up to date? Backups?