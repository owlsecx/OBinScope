# 🦉 OBinScope

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OBinScope** — Static Executable Triage Analyzer

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Static executable triage analyzer — PE / ELF / Mach-O headers, mitigations, packers, IOCs

---

## ✨ Features

- Hand-parsed PE / ELF / Mach-O (incl. FAT) via struct
- Mitigations, imports, packers, entropy, strings/IOCs
- Embedded PE/ELF detection, fuzzy profile, Authenticode
- Verdict + A+…F grade with MITRE ATT&CK / CAPEC tags
- Exports TXT/MD/JSON/CSV/SARIF · --demo · full CLI

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OBinScope
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
