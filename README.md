# 🦉 OUnboundX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OUnboundX** — Unbound DNS Resolver Hardening Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview


OUnboundX is an offline, read-only Unbound DNS resolver configuration auditor that parses unbound.conf with include globs, stanza awareness and full continuation support. It evaluates access-control exposure, remote-control (unbound-control) security, DNSSEC and QNAME minimisation, cache-poisoning hardening and TLS/DoT settings. Findings are mapped to CWE and MITRE ATT&CK, scored and graded, and exported as TXT, Markdown, JSON, CSV or SARIF.

---

## ✨ Features


- Stdlib unbound.conf parser with include/include-toplevel globs, stanzas and continuations
- Access-control audit: open resolver (0.0.0.0/0 allow), missing default deny, interface 0.0.0.0 exposure
- remote-control checks: control-enable, control-interface bind, control-use-cert and key file perms
- DNSSEC (auto-trust-anchor/trust-anchor, val-permissive), QNAME minimisation and 0x20 randomisation
- Cache-poisoning hardening (harden-*), rrset/msg cache sizing, DoT upstreams and private-address leaks
- CWE+ATT&CK mapping, offline --root trees, score/grade and TXT/MD/JSON/CSV/SARIF export

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OUnboundX --scan -f sarif -o unbound.sarif
./OUnboundX -c /etc/unbound/unbound.conf --min-severity medium
./OUnboundX -r /mnt/image --fail-on high --json
./OUnboundX --demo
./OUnboundX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled.s.Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
