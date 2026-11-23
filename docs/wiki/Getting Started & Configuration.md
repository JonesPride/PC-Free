# PC-Free — Getting Started & Configuration

## Current documentation source
The README contains a Codespaces walkthrough, manual Docker instructions, and a sample `windows10.yml` Compose definition. Separate root Compose files were not found at the expected names during source review.

## README setup outline
1. Fork the repository as the README instructs.
2. Create a Codespace or prepare a local Docker host.
3. Review available storage and Docker data-root instructions.
4. Configure Windows username/password and resource settings.
5. Start the Windows container using the documented Compose example.
6. Access the web console through the configured browser port.

## Configuration values shown
The README example includes Windows version, username, password, RAM size, CPU cores, disk size, ports 8006/3389, and persistent volume mappings.

## Important caution
Do not treat the README as a verified current deployment recipe until the actual tracked Compose/config files and current upstream image requirements are inspected. The README's port-visibility instructions conflict; keep access private unless a separate security review approves exposure.