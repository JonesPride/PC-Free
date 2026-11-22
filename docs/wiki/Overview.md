# PC-Free — Overview

## Purpose and scope
PC-Free is documented as an open-source project for running a Windows environment in a browser using Docker and GitHub Codespaces, without requiring a local Windows PC.

## Documented components and features
- Docker Compose configuration using the `dockurr/windows` image.
- Windows 10 configuration, with README options for Windows 11.
- Browser access through the web interface/noVNC.
- Optional Remote Desktop Protocol port mapping.
- Docker volumes for Windows data persistence.
- Environment-variable configuration for username, password, memory, CPU, and disk size.
- Codespaces and local Docker setup instructions.

## Requirements documented
For Codespaces: GitHub account, modern browser, available storage, and stable internet. For local Docker: Docker Engine, disk space, RAM, and virtualization support such as KVM/Hyper-V.

## Important cautions
The README includes destructive cleanup instructions using `docker-compose down -v`; this removes volumes and Windows data. Treat this as a destructive operation. Secrets belong in an untracked environment file, not source control.

## Validation boundary
The README contains setup and troubleshooting instructions, but this documentation pass has not independently tested the deployment, Windows licensing, persistence, security isolation, or current Codespaces compatibility.