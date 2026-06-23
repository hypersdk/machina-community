# Machina — Community

> **Enterprise Linux hypervisor management — libvirt/QEMU/KVM, web UI, VNC/SPICE consoles**

Public issue tracker and community feedback space for **Machina** by [Zyvor AI Labs](https://zyvor.dev).

The source code is maintained in a private repository. This repo is for:
- Bug reports
- Feature requests
- UX feedback
- Documentation gaps
- Questions and discussion

---

## Key features

- Full VM lifecycle — create, start, stop, snapshot, migrate, clone
- Built-in noVNC, SPICE, serial, and SSH console proxies
- Web UI (React 19 + xterm.js) + TUI (ratatui) + REST API + machinactl CLI
- Prometheus metrics, PSI/cgroups monitoring, alerts, webhooks
- PAM auth + RBAC
- Optional KubeVirt migration path
- PacketWolf integration for VM network visibility

---

## Installation

Machina runs on any Linux bare-metal node with libvirt/KVM.

**One-command deploy:**
```bash
git clone https://github.com/hypersdk/machina && cd machina
./machinactl deploy   # installs deps, builds, installs as systemd service, verifies

# Open https://localhost:5092
# Or run the TUI:
machina
```

**Remote deploy:**
```bash
./scripts/deploy-remote.sh HOST USER
./scripts/package-binary-remote.sh HOST USER --fetch
```

**Requirements:** Linux (Ubuntu 22.04+ / Rocky 9), libvirt + QEMU/KVM installed, 4 GB RAM

---

## Report a bug

[Open a Bug Report →](../../issues/new?template=bug_report.yml)

Include: what you did, what happened, what you expected, your environment, and screenshots/logs (redact secrets).

## Request a feature

[Open a Feature Request →](../../issues/new?template=feature_request.yml)

## UX feedback

[Open a UX Feedback →](../../issues/new?template=ux_feedback.yml)

## Ask a question

Use [GitHub Discussions](../../discussions) for open-ended questions, ideas, and roadmap conversations.

---

## Security

**Do not report security vulnerabilities publicly.**

Email **security@zyvor.dev** — see [SECURITY.md](SECURITY.md).

---

## Do not post

- Source code or internal configuration
- API tokens, license keys, or credentials  
- Private logs with sensitive data
- Security vulnerabilities (email security@zyvor.dev)

---

Maintained by [Zyvor AI Labs](https://zyvor.dev)
