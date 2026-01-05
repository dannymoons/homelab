# Homelab Configuration

Docker configurations for my homelab services running on a **UGREEN DXP4800 Plus** NAS.

## Hardware

- **NAS**: UGREEN DXP4800 Plus
- **Network**: All services connected via Tailscale for secure remote access

## Services

- [Home Assistant](docker/home-assistent/): Home automation platform for smart home
- [Immich](docker/immich-ts/): Self-hosted photos and videos solution with machine learning
- [Jellyfin](docker/jellyfin-ts/): Media server for streaming movies, TV shows, and music
- [Glance](docker/glance-ts/): Customizable dashboard for monitoring services

## Network Architecture

All services are exposed through Tailscale sidecars (`-ts` suffix) for secure remote access without exposing ports to the public internet. Each service runs in a Docker container with its network traffic routed through a Tailscale companion container.