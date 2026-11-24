# 🦉 OBinScope

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OBinScope** — Static Executable Triage Analyzer

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OBinScope is a static executable triage analyzer for PE, ELF and Mach-O (including FAT) binaries that is strictly read-only and never executes, loads or emulates a sample. Every header is parsed by hand with the stdlib struct module, and it extracts mitigations, imports, packer indicators, entropy, strings and IOCs with no network I/O. It produces a verdict and an A+…F grade tagged with MITRE ATT&CK/CAPEC references.

---

## ✨ Features

- Hand-parsed PE / ELF / Mach-O / FAT headers via stdlib struct (no execution)
- Mitigation, import, packer and entropy/packing analysis
- Strings sampling and IOC extraction
- Embedded PE/ELF detection and Authenticode awareness
- Verdict and A+…F grade with MITRE ATT&CK / CAPEC tags
- Export TXT/MD/JSON/CSV/SARIF with --demo self-test and CI fail-on

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OBinScope --path suspicious.exe
./OBinScope -p ./samples/ --iocs --entropy --format-out json -o report.json
./OBinScope --demo
./OBinScope --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OBinScope --help   # watch every network call
firejail --net=none ./OBinScope --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
