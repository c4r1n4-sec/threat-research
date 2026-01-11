# Threat Research 🔬

Deep dives into malware, attack techniques, and adversary tactics. I tear apart samples to understand their execution chains, document evasion techniques, and build detection rules.

This repo is part of my continuous learning process and each analysis introduces new reverse engineering techniques, tools, and detection methodologies. I document everything as I figure it out.

Since I am constantly refining my skills, I gladly accept criticism and advice. If you see a better way to analyze a sample or improve a detection rule, I would love to hear from you.

This is ongoing work. As I finish each analysis, I'll link it here and keep adding new samples.

---

## 📚 Analyses

### 🎭 [Lumma Stealer](./Lumma-Stealer/)
**Static analysis of AutoIt loader + network forensics from PCAP**

Post-takedown sample showing how Lumma survived the May 2025 Microsoft/DOJ operation. Decompiled the AutoIt loader, decoded COMMONS obfuscation, and performed PCAP forensics on Brad Duncan's real-world capture to analyze C2 fingerprinting and encrypted payload delivery.

**Techniques:** AutoIt decompilation, string decoding, infection chain mapping, PCAP analysis, TLS SNI inspection

---

### 🔒 [LockBit 3.0](./LockBit-3.0/)
**Fileless ransomware using PowerShell reflective DLL injection**

Extracted payload from memory mid-execution, reverse engineered the API hashing algorithm (XOR 0x11039ffe), and documented WMI-based shadow copy deletion that bypasses command-line monitoring.

**Signature:** aPLib compression (BlackMatter lineage) | **Evasion:** Stack string obfuscation, offline encryption

---

### 🦠 [RedLine Stealer](./redline-stealer/)
**Info stealer exploiting Windows DPAPI to decrypt browser passwords**

Campaign targeted game cheat forums (campaign ID: "cheat"). Built automated IOC extraction tooling and documented the SOAP-based C2 beacon pattern.

**Key Finding:** Chrome's DPAPI protection is meaningless when malware runs as your user

---

## 🔧 Tools I Use

- **FLARE-VM** - Windows malware analysis
- **REMnux** - Linux analysis toolkit
- **Ghidra** - Reverse engineering
- **Wireshark** - Network analysis
- **dnSpy** - .NET decompilation
- **Hollows Hunter** - Memory forensics
- **FLOSS/CAPA** - String extraction & capability analysis
