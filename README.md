# Threat Research 🔬

Deep dives into malware, attack techniques, and adversary tactics. I tear apart samples to understand their execution chains, document evasion techniques, and build detection rules.

This repo is part of my continuous learning process. Each analysis introduces new reverse engineering techniques, tools, and detection methodologies. I document everything as I figure it out.

This is ongoing work. As I finish each analysis, I'll link it here and keep adding new samples.

---

## 📚 Analyses

### 🦠 [RedLine Stealer](./RedLine-Stealer/)

Info stealer exploiting Windows DPAPI to decrypt browser passwords. Campaign targeted game cheat forums (campaign ID: "cheat"). Unpacked from memory, reverse engineered the DPAPI exploitation, and built IOC extraction tooling.

**C2:** `185.222.58.54:55615` | **Protocol:** SOAP | **Tools:** Hollows Hunter, dnSpy, Wireshark

---

### 🔒 [LockBit 3.0](./LockBit-3.0/)

Fileless ransomware using PowerShell reflective DLL injection. Extracted payload from memory mid-execution, reverse engineered the API hashing algorithm (XOR 0x11039ffe), and documented WMI-based shadow copy deletion that bypasses command-line monitoring.

**Signature:** aPLib compression (BlackMatter lineage) | **Evasion:** Stack string obfuscation, offline encryption | **Tools:** Hollows Hunter, Ghidra, FLOSS

---

### 🔄 Lumma Stealer *(In Progress)*

MaaS infostealer using AutoIt loader chains and fake CAPTCHA delivery. Analyzing post takedown (May 2025) sample showing persistence and adaptation after infrastructure disruption.

**Sample Date:** January 2026 | **Distribution:** Cracked software | **Techniques:** AutoIt obfuscation, multi-stage loader

---

## 🛠️ Tools

FLARE-VM, REMnux, Wireshark, dnSpy, Hollows Hunter, System Informer, Ghidra, YARA, Python
