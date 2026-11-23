# PC-Free — Security & Operations

## Credentials
The README instructs users to place Windows credentials in `.env` and add it to `.gitignore`. The root ignore file was not found at the queried path during this review. Verify the actual ignore rules before entering credentials.

## Network exposure
The README contains conflicting guidance about port 8006 visibility, including an instruction to make it Public in troubleshooting. Do not expose a Windows desktop publicly without authentication, access restrictions, and a deliberate threat review.

## Destructive cleanup
The documented `docker-compose ... down -v` command deletes the container's persistent volumes and Windows data. Do not run it as a routine troubleshooting step.

## Upstream and licensing
This project relies on the third-party `dockurr/windows` image and Windows installation. Verify upstream behavior and Microsoft licensing requirements for the intended use. The README's free-cost and security claims are not independent guarantees.