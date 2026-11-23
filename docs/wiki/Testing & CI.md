# PC-Free — Testing & CI

## Current evidence
The README contains manual setup and troubleshooting steps but does not document a dedicated automated test suite or CI workflow.

## Manual verification required
- Confirm Docker Engine and virtualization support on the target host.
- Verify the actual Compose file and container image version.
- Start and stop the environment.
- Confirm browser access and optional RDP behavior.
- Restart the container and verify volume persistence.
- Perform a backup and restore test before relying on stored data.

## Not verified
No Codespaces deployment, Windows boot, browser session, RDP session, performance, or restore test was performed during this documentation pass.