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

Offline Unbound DNS resolver configuration hardening auditor

---

## ✨ Features

- Stdlib unbound.conf parser — clauses, quoting, comments, include: / include-toplevel: with globs, unbound.conf.d
- Open-resolver detection (interface × access-control)
- Identity / version hiding, minimal-responses, deny-any
- harden-* family, qname-minimisation, 0x20, aggressive-nsec
- DNSSEC — validator module, trust anchors, permissive mode, domain-insecure, root-key-sentinel, val-clean-additional
- DNS rebinding — private-address / private-domain coverage
- ratelimit / ip-ratelimit / unwanted-reply-threshold
- chroot / username / directory / pidfile / logfile
- remote-control — interface, certificates, key permissions
- forward-zone / stub-zone TLS upstream, tls-cert-bundle
- DoT / DoH server keys, http-notls-downstream, ciphers
- root-hints freshness, file ownership / permissions
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OUnboundX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
