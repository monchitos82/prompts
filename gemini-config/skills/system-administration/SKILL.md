---
name: system-administration
description: >
  Workflow and safety checklist for Linux system administration, service
  management, networking, storage, and server troubleshooting.
---

# System Administration Skill

## Inspect Before Mutating
- Check service state, logs, disk space, memory, and network sockets first (`systemctl status`, `journalctl -xeu <unit>`, `df -h`, `free -h`, `ss -tulpn`, `ip addr`).
- Read existing configuration files and back them up or diff changes in version control before editing.

## Execute Safely
- Prefer idempotent commands and explicit flags over interactive prompts or implicit defaults.
- State the blast radius before running destructive or service-disrupting commands (`rm -rf`, `systemctl restart`, firewall rule changes, mount/partition edits).
- Validate configuration syntax before reloading or restarting services (`nginx -t`, `sshd -t`, `systemd-analyze verify`).

## Verify and Report
- Confirm active service status, listening ports, permissions, and log output after applying changes.
- Summarize what changed, why it was needed, any remaining risks, and the exact verification commands run.
