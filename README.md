> 🚀 **Trial v0.30.0 is live!** The latest release is available for trial today — [get started in 5 minutes →](#try-v030-in-5-minutes)

# Machina — Community

> **Enterprise Linux hypervisor management — libvirt/QEMU/KVM, web UI, VNC/SPICE consoles, REST API.**

![Version](https://img.shields.io/badge/version-v0.30.0-blue) ![Discussions](https://img.shields.io/github/discussions/hypersdk/machina-community) ![Issues](https://img.shields.io/github/issues/hypersdk/machina-community) ![License](https://img.shields.io/badge/license-Proprietary-red)

Public issue tracker and community feedback space for **Machina** by [Zyvor AI Labs](https://zyvor.dev).
The source code is maintained in a private repository. This repo is for bug reports, feature requests, UX feedback, and community discussion.

---

## What's new in v0.30

- SPICE console GA — full clipboard, USB redirect, and audio passthrough in the browser
- Batch snapshot — snapshot all VMs in a pool in parallel with one CLI command
- Node pool scheduler — pin VM groups to hardware pools with affinity rules
- Remote deploy one-liner: `curl -fsSL https://get.hypersdk.dev/machina | bash`
- Prometheus exporter v0.30 — 40+ new metrics including per-VM PSI pressure

---

## Why Machina

| Problem | Machina answer |
|---------|---------------|
| virsh scripts scatter VM ops across dozens of commands | One REST API and dashboard for the full VM lifecycle |
| Browser consoles need separate noVNC gateways | Built-in noVNC, SPICE, serial, and SSH proxies — no extra setup |
| No fleet observability without custom Prometheus setup | Embedded exporter — 40+ metrics, alerts, PSI/cgroups out of the box |
| KubeVirt migration means rewriting all automation | Documented YAML bundle migration path — move at your own pace |
| Vendor hypervisor lock-in | Open-source Rust daemon — runs on your metal, no license fees |

---

## Architecture

```
┌──────────────────────────────────────────────────────────────┐
│  Interfaces   Web UI · TUI · REST API · machinactl CLI       │
├──────────────────────────────────────────────────────────────┤
│  Daemon       machina-daemon — PAM · RBAC · console proxies  │
├──────────────────────────────────────────────────────────────┤
│  Hypervisor   libvirt · QEMU/KVM · optional KubeVirt path    │
└──────────────────────────────────────────────────────────────┘
```

---

## Try v0.30 in 5 minutes

```bash
# One-command install on any Linux node with KVM
curl -fsSL https://get.hypersdk.dev/machina | MACHINA_VERSION=0.30.0 bash

# Or build from source
git clone https://github.com/hypersdk/machina && cd machina
./machinactl deploy

# Open https://localhost:5092 or launch the TUI:
machina
```

**Requirements:** Linux (Ubuntu 22.04+ / Rocky Linux 9), libvirt + QEMU/KVM, 4 GB RAM

---

## Report a bug

[Open a Bug Report →](../../issues/new?template=bug_report.yml)

Include: what you did, what happened, what you expected, your environment, screenshots or logs (redact secrets).

## Request a feature

[Open a Feature Request →](../../issues/new?template=feature_request.yml)

## UX feedback

[Open a UX Report →](../../issues/new?template=ux_feedback.yml)

## Ask a question

Use [GitHub Discussions](../../discussions) for open-ended questions, ideas, and roadmap conversations.

---

## Security

**Do not report security vulnerabilities publicly.**
Email **security@zyvor.dev** — see [SECURITY.md](SECURITY.md).

---

## Do not post

- Source code, internal configs, or architecture details
- API tokens, license keys, or credentials
- Private logs with sensitive data
- Security vulnerabilities — email security@zyvor.dev instead

---

## Join the community

⭐ [Star this repo](https://github.com/hypersdk/machina-community) · 💬 [Open a Discussion](https://github.com/hypersdk/machina-community/discussions) · 🐛 [Report a Bug](../../issues/new?template=bug_report.yml) · 📧 [hello@zyvor.dev](mailto:hello@zyvor.dev)

Maintained by [Zyvor AI Labs](https://zyvor.dev)
