# PC-Free — Overview

## Purpose and scope
The repository README presents PC-Free as a way to run a Windows 10 environment in a browser through GitHub Codespaces or a local Docker host, using the upstream `dockurr/windows` container image. It describes optional Windows 11 configuration, browser/noVNC access, optional RDP, and persistent Docker volumes.

## What the README documents
- Codespaces and manual Docker setup walkthroughs.
- A sample `windows10.yml` Compose configuration embedded in the README.
- Environment variables for Windows username/password and resource allocation (RAM, CPU, disk).
- Browser access through port 8006 and optional RDP through port 3389.
- A named `windows-data` volume and a host data-root mapping in the sample YAML.
- Startup, stop, restart, logs, resource tuning, troubleshooting, and destructive removal commands.
- A roadmap that lists some features as completed and others as planned.

## Source verification limits
During this review, the README was available, but fetches for root-level `windows10.yml`, `docker-compose.yml`, `docker-compose.yaml`, and `compose.yaml` returned not found. Therefore the Compose content is documented as a README example, not verified as a separately tracked deployment file. Runtime deployment, actual Codespaces compatibility, container behavior, licensing, and backup/restore have not been tested.

## Security and destructive operations
- The README instructs users to put credentials in `.env` and add it to `.gitignore`; the actual ignore file was not found at the queried root path during this pass.
- Port visibility instructions are inconsistent: most setup steps imply browser access, while a troubleshooting section says to make port 8006 Public. Do not expose the service publicly without a separate security and access review.
- `docker-compose ... down -v` is explicitly destructive and deletes Windows data volumes.
- README claims such as “100% free,” “5-minute setup,” and security isolation are project claims, not independently verified guarantees.

## Status
This is README-led documentation only until the actual tracked deployment files and current repository tree can be inspected.

## Source basis
Default-branch README. Missing paths are recorded as unverified rather than inferred from the README's embedded YAML.