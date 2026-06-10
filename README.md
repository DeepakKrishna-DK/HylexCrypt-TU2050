# HylexCrypt - The Ultimate 2050
![HylexCrypt Logo](https://github.com/TwinCiphers/HylexCrypt-TU2050/blob/main/docs/Logo.jpeg)
> 🔐 Unified Advanced Steganography + Cryptography Tool (Educational & Research Use)

HylexCrypt - The Ultimate 2050 is an **all-in-one steganography and encryption toolkit**.  
It encrypts secret messages with modern cryptographic algorithms and hides them inside files (images, audio, etc.) using steganography — producing normal-looking files that secretly contain secure information.

---
## 📖 Documentation & Publication
View the Complete Documentation here [HylexCrypt-Docs](https://hackmd.io/@hylexcrypt-tu2050/SkRnM51ogl) <br>
Publication: [<img width="191" height="20" alt="image" src="https://github.com/user-attachments/assets/2596a8d6-a74e-42e3-b58d-4ea6de9f0465" />](https://doi.org/10.5281/zenodo.20622278)
Published research artifact available on Zenodo.

## Authors
Author Name: DEEPAK P S <br>
Mail id: deepakkrishnark@gmail.com 

Author Name: NITHIN S <br>
Mail id: nithinsrinivas333@gmail.com

## ✨ Features

- **🔑 Argon2id Key Derivation** – Memory-hard KDF, secure against brute-force.
- **🛡️ Authenticated Encryption** – AES-256-GCM & ChaCha20-Poly1305 (AEAD).
- **🖼️ Steganography** – LSB (Least Significant Bit) embedding for PNG/audio.
- **♻️ Error Correction** – Reed–Solomon forward error correction for resilience.
- **⏳ Self-destruct Messages** – Expiry timestamp and scheduled wipe options.
- **🖥️ Device Locking** – Bind ciphertexts to machine/device + pepper file.
- **🧪 Self-test Suite** – Built-in verification of crypto and stego functions.
- **⚡ Cross-platform** – Works on Linux, Windows, macOS (Python ≥ 3.9).

---

## 📥 Installation

### Requirements
- Python 3.9+
- Pip and virtual environment recommended.

### Steps
```bash
git clone https://github.com/TwinCiphers/HylexCrypt-TU2050.git
cd hylexcrypt
pip install -r requirements.txt
Dependencies include: pillow, numpy, cryptography, argon2-cffi, reedsolo, scipy, soundfile, psutil, colorama.

## 🚀 Usage

### General format:

hylexcrypt <command> [options]

Encode a message: 
hylexcrypt encode carrier.png -o outdir -m "Top Secret" -p "StrongPass!2025"

Encode with expiry (in 1 to 86400 seconds):
hylexcrypt encode carrier.png -o outdir -m "Ephemeral" -p "StrongPass!2025" --expire 60

Decode a message:
hylexcrypt decode outdir/carrier_stego.png -p "StrongPass!2025"

Wipe hidden message:
hylexcrypt wipe-message outdir/carrier_stego.png

Schedule a wipe (after 120 seconds):
hylexcrypt encode carrier.png -o outdir -m "AutoWipe" -p "Pass!" --autowipe 120

Run self-tests:
hylexcrypt selftest

Manual / Help:
hylexcrypt manual
hylexcrypt <command> -h

🔒 Security Notes:

 -- Password safety – Avoid passing -p inline; omit to be prompted securely.
 -- Pepper file – pepper.txt is unique to your device; 
    losing it means you can’t decrypt device-locked  messages.
 -- Message expiry – Expired messages cannot be recovered.
 -- FEC protection – Reed–Solomon ensures recovery from minor image/audio corruption.
 -- Use strong passphrases – Length > 12 chars recommended (per NIST).

 Project Structure:

 hylexcrypt/
 ├── cli.py                # CLI commands
 ├── core.py               # Core crypto & stego logic
 ├── __init__.py           # Package init
Legal_docs/
 ├── LICENSE               # Apache-2.0 license
 ├── NOTICE.txt            # Notices & attribution
 ├── SECURITY.md           # Security reporting policy
 ├── AUP.md                # Acceptable Use Policy
 ├── CLA.md                # Contributor License Agreement
 ├── EXPORT_COMPLIANCE.md  # Export control info
 ├── FIPS_EXPORT.md        # FIPS compliance notes
pepper.txt                 # Device-specific secret 
requirements.txt           # Dependencies
pyproject.toml             # Build config


⚖️ License:

This project is released under a license:
Apache License 2.0
Note: Illegal, unethical, or malicious use of this software is strictly prohibited.
See Legal_docs/
 for full texts and compliance information.

👥 Governance:

Founders and Maintainers: TwinCiphers (see NOTICE.txt)
Contributors: Must sign CLA.md before merging PRs.

🌍 Export & Compliance:

HylexCrypt includes strong encryption.
Users/distributors must ensure compliance with:
-- India: Governed under [DGFT & IT Act]
-- International: U.S. EAR export controls for cryptography
FIPS: See Legal_docs/FIPS_EXPORT.md for details.


📖 Resources:
Argon2 Password Hashing
AES-GCM Mode Overview
ChaCha20-Poly1305 RFC 8439
Reed–Solomon Codes

### ⚠️ Disclaimer  
This project is for **educational and lawful security research only** (as this is the starting phase).  
The authors and contributors are **not liable for misuse**.
