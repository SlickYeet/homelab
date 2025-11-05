# Proxmox Homelab

A self-hosted infrastructure running on a single Proxmox node built from
recycled PC hardware. This setup demonstrates automation, virtualization,
service orchestration, and secure networking — all managed and monitored
locally.

## Stack Overview

- **Proxmox VE:** Base hypervisor
- **Cloudflare DDNS:** Dynamic DNS updates for public access
- **Nginx Proxy Manager:** Reverse proxy + SSL
- **AdGuard Home:** DNS filtering + ad blocking
- **Coolify / Dokploy:** Local deployment platforms
- **MinIO:** S3-compatible object storage
- **Pelican Panel + Wings:** Game server hosting
- **WireGuard:** VPN access
- **TrueNAS:** File and media storage
- **Jellyfin + [arr*]:** Automated media management
- **Uptime Kuma:** Service uptime tracking

## Architecture

![Architecture Diagram](docs/architecture-diagram.png)

## Automation

- Automatic DNS updates via Cloudflare API
- Periodic backups of all active services

## Security

- All inbound traffic routed through Cloudflare + Nginx Proxy Manager
- Strict internal DNS with AdGuard
- WireGuard VPN for secure admin access

## Monitoring

- Uptime Kuma for availability checks
- Centralized dashboard showing uptime and metrics

## Future Plans

- Expand Proxmox cluster to at least 3 nodes
- Seperate Proxmox from main network
