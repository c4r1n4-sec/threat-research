# Threat Research 🔬

Deep dives into malware, attack techniques, and adversary tactics. I tear apart samples to understand their execution chains, document evasion techniques, and build detection rules.

This repo is part of my continuous learning process - each analysis introduces new reverse engineering techniques, tools, and detection methodologies. I document everything as I figure it out.

This is ongoing work. As I finish each analysis, I'll link it here and keep adding new samples.

---

## 📚 Analyses

### 🎭 [Lumma Stealer](./lumma-stealer/)
**AutoIt loader with process hollowing and network traffic forensics**

Post-takedown sample showing how Lumma survived the May 2025 Microsoft/DOJ operation. COMMONS obfuscation, JavaScript fingerprinting, and encrypted follow-up malware downloads. The malware evolved from credential stealer to initial access loader.

**Techniques:** AutoIt obfuscation, process hollowing, C2 fingerprinting, TLS evasion

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
