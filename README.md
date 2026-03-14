<div align="center">

# 🦉 OBurrow

**Local File Inclusion Hunter**

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

*Part of the [OwlSec](https://owlsec.org) Toolkit*
```
██████╗ ██████╗ ██╗   ██╗██████╗ ██████╗  ██████╗ ██╗    ██╗
██╔═══██╗██╔══██╗██║   ██║██╔══██╗██╔══██╗██╔═══██╗██║    ██║
██║   ██║██████╔╝██║   ██║██████╔╝██████╔╝██║   ██║██║ █╗ ██║
██║   ██║██╔══██╗██║   ██║██╔══██╗██╔══██╗██║   ██║██║███╗██║
╚██████╔╝██████╔╝╚██████╔╝██║  ██║██║  ██║╚██████╔╝╚███╔███╔╝
 ╚═════╝ ╚═════╝  ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝ ╚═════╝  ╚══╝╚══╝
              Traversal | Encode | Diff | Fuzz | Report
```

</div>

---

## 📌 Overview

**OBurrow** is an LFI (Local File Inclusion) vulnerability scanner for authorized security testing. It supports multiple encoding bypass techniques, PHP wrapper injection, and blind LFI detection via response diff analysis.

---

## 🖥️ Modules

| Option | Module | Description |
|--------|--------|-------------|
| `[1]` | Standard Scan | Full LFI scan with configurable profiles |
| `[2]` | Single Test | Test one path across all encoding methods |
| `[3]` | Payload Gen | Generate and export custom payload lists |
| `[4]` | Path Viewer | Browse the built-in sensitive path library |
| `[5]` | History | View past scan sessions |

---

## 🔤 Encoding Methods

| Encoding | Description |
|----------|-------------|
| `none` | Raw payload — no encoding |
| `url` | Standard URL encoding |
| `double_url` | Double URL encoding bypass |
| `null_byte` | Append `%00` — old PHP null byte bypass |
| `unicode` | Unicode slash bypass |
| `backslash` | Windows path separator `\` |

---

## 🔍 Diff Mode

OBurrow fetches a baseline 404-like response, then flags any payload that returns a significantly different response size — enabling detection of **blind LFI** vulnerabilities where content isn't directly reflected.

---

## 🐘 PHP Wrappers

| Wrapper | Purpose |
|---------|---------|
| `php://filter` | Read source code (base64 encoded) |
| `data://` | Inject PHP code into the request |
| `expect://` | Command execution (if enabled on server) |

---

## 📁 Output Files

| File | Description |
|------|-------------|
| Text report | Generated after each scan |
| JSON export | Full scan results in JSON format |
| `~/.oburrow_history.json` | Persistent scan history |

---

## ⚙️ Requirements

- Linux (any distro)
- The tool is pre-built — no Python installation needed

---

## ⚠️ Legal Disclaimer

> **THIS TOOL IS FOR EDUCATIONAL AND AUTHORIZED AUDIT PURPOSES ONLY.**  
> Never use against systems without explicit written permission.  
> Unauthorized testing is illegal and unethical.  
> The developer is not responsible for any misuse.

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

> 🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
