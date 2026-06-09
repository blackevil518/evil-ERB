# 🛡️ evil-ERB

### *Educational Ransomware Blueprint – Learn Offensive Security the Right Way*

[![GitHub contributors](https://img.shields.io/github/contributors/blackevil518/evil-ERB?style=for-the-badge&color=blue)](https://github.com/blackevil518/evil-ERB/graphs/contributors)
[![GitHub forks](https://img.shields.io/github/forks/blackevil518/evil-ERB?style=for-the-badge&color=green)](https://github.com/blackevil518/evil-ERB/network)
[![GitHub stars](https://img.shields.io/github/stars/blackevil518/evil-ERB?style=for-the-badge&color=yellow)](https://github.com/blackevil518/evil-ERB/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/blackevil518/evil-ERB?style=for-the-badge&color=red)](https://github.com/blackevil518/evil-ERB/issues)
[![MIT License](https://img.shields.io/github/license/blackevil518/evil-ERB?style=for-the-badge)](https://github.com/blackevil518/evil-ERB/blob/main/LICENSE)
[![Python 3.10+](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python)](https://www.python.org/)

</div>

---

## 📌 Table of Contents
- [🔥 Introduction](#-introduction)
- [✨ Features](#-features)
- [⚠️ Drawbacks & Risks (Ethical Warning)](#️-drawbacks--risks-ethical-warning)
- [💻 System Requirements](#-system-requirements)
- [🛠️ Installation Guide](#️-installation-guide)
  - [🐧 Kali Linux / Debian-based](#-kali-linux--debian-based)
  - [🪟 Windows 10/11](#-windows-1011)
  - [🍎 macOS](#-macos)
- [🚀 Usage](#-usage)
- [📁 Project Structure](#-project-structure)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)
- [📞 Contact](#-contact)

---

## 🔥 Introduction

**evil-ERB** is an **educational toolkit** designed to simulate and analyze ransomware-like behavior **in a fully isolated environment**. It helps security students, blue teamers, and malware analysts understand:

- How file encryption/decryption works (simulated)
- Ransomware persistence mechanisms
- Behavioral detection & forensic analysis

> 🛑 **This project is for LEARNING and RESEARCH only.**  
> The author is **not responsible** for any misuse. Always run this inside a **virtual machine** or **air-gapped lab**.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| ✅ **Simulated Encryption** | Uses AES (simulated) to "lock" dummy files in a test folder. |
| ✅ **Ransom Note Generator** | Creates a realistic ransom note (educational purposes only). |
| ✅ **Decryption Module** | Demonstrates how proper key management allows recovery. |
| ✅ **Cross-platform** | Works on Windows, Linux (Kali), and macOS. |
| ✅ **Logging & Analysis** | Logs every action for forensic study. |
| ✅ **Configurable** | Easily change file extensions, target directories, etc. |
| ✅ **Virtual Environment Ready** | Safe to run inside Docker / VM. |

---

## ⚠️ Drawbacks & Risks (Ethical Warning)

> **Read this carefully before using evil-ERB.**

| Drawback / Risk | Explanation |
|----------------|-------------|
| 🧨 **Real damage if misused** | If run on real files (not dummy targets), it can permanently encrypt your data. |
| 🚫 **No real decryption guarantee** | This is a simulation – not a production recovery tool. |
| ⚡ **Antivirus false positives** | Many AVs flag ransomware simulations as malware. You must whitelist the folder. |
| 🔐 **Requires isolated environment** | Running on your host OS can accidentally affect important files. **Always use a VM**. |
| 🧠 **Educational only – not for attacks** | Using this against any system without permission is **illegal**. You are solely responsible. |

> ✅ **Best practice:**  
> - Use **Kali Linux** inside **VirtualBox** or **VMware**.  
> - Create a dedicated `test_folder` with dummy `.txt` files.  
> - Never point the tool to `C:\`, `/home`, or any real data.

---

## 💻 System Requirements

- **Python 3.10+**
- `pip` package manager
- **Virtualization software** (VMware / VirtualBox) – strongly recommended
- OS: Windows 10/11, Kali Linux 2023+, macOS 12+

---

## 🛠️ Installation Guide

### 🐧 Kali Linux / Debian-based

```bash
# 1. Update system
sudo apt update && sudo apt upgrade -y

# 2. Install Python3 and venv if missing
sudo apt install python3 python3-venv python3-pip -y

# 3. Clone repository
git clone https://github.com/blackevil518/evil-ERB.git
cd evil-ERB

# 4. Create virtual environment
python3 -m venv venv
source venv/bin/activate

# 5. Install dependencies
pip install -r requirements.txt

# 6. (Optional) Create a safe test folder
mkdir test_encryption_lab
```

---

### 🪟 Windows 10/11

```powershell
# 1. Install Python 3.10+ from python.org (check "Add to PATH")

# 2. Open PowerShell as Administrator
Set-ExecutionPolicy Unrestricted -Scope CurrentUser -Force

# 3. Clone the repo
git clone https://github.com/blackevil518/evil-ERB.git
cd evil-ERB
python main.py
# 4. Create virtual environment
python -m venv venv
.\venv\Scripts\activate

# 5. Install requirements
pip install -r requirements.txt

# 6. Create test folder (in isolated drive like D:\testlab or desktop\testlab)
mkdir C:\evil_ERB_lab
```

> 💡 **Windows Defender may quarantine files.** Add the project folder to exclusions before running.

---

### 🍎 macOS

```bash
# 1. Install Homebrew (if not already)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# 2. Install Python3
brew install python@3.10

# 3. Clone and setup
git clone https://github.com/blackevil518/evil-ERB.git
cd evil-ERB
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# 4. Create safe test area
mkdir ~/evil_ERB_sandbox
```

---

## 🚀 Usage

### 1. Prepare a Safe Test Environment

- Create a folder with **dummy files** (e.g., `test.txt`, `document.docx` – make copies).
- Never run this on real personal or system files.

### 2. Run the Main Script

```bash
python main.py --target ./test_encryption_lab --simulate
```

Arguments:

| Argument | Description |
|----------|-------------|
| `--target` | Path to the test folder (default: `./testlab`) |
| `--simulate` | Dry-run mode (no actual changes, just logs) |
| `--encrypt` | Perform simulated encryption |
| `--decrypt` | Restore encrypted dummy files (if key is available) |

### 3. Example Workflow (Educational)

```bash
# Dry-run first
python main.py --target ./sandbox --simulate

# Simulate encryption
python main.py --target ./sandbox --encrypt

# Simulate decryption
python main.py --target ./sandbox --decrypt
```

### 4. Analyze Logs

All actions are logged in `evil_erb.log`. Use it for forensic exercises.

---

## 📁 Project Structure

```
evil-ERB/
├── main.py                 # Entry point
├── ransomware.py           # Core encryption/decryption logic
├── ransomware_builder.py   # Configuration builder
├── worker.py               # Background worker simulation
├── requirements.txt        # Dependencies (colorama, cryptography, etc.)
├── evil_erb.log            # Log file (auto-generated)
├── config.json             # Settings (target extensions, note text)
├── docs/                   # Additional educational resources
│   └── forensic_guide.md
└── README.md               # This file
```

---

## 🤝 Contributing

Contributions are welcome! Help improve educational content, add detection mechanisms, or fix bugs.

1. Fork the repository.
2. Create your feature branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m 'Add amazing feature'`
4. Push: `git push origin feature/amazing-feature`
5. Open a Pull Request.

Please follow the [Code of Conduct](CODE_OF_CONDUCT.md) (if added).

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.

This means you can freely use, modify, and distribute the code for educational purposes, but the author assumes **no liability** for misuse.

---

## 📞 Contact

- **Project Maintainer:** [@blackevil518](https://github.com/blackevil518)
- **Project Link:** [https://github.com/blackevil518/evil-ERB](https://github.com/blackevil518/evil-ERB)
- **Report Issues:** [GitHub Issues](https://github.com/blackevil518/evil-ERB/issues)

---

## 🙏 Acknowledgments

- The cybersecurity open-source community
- Python `cryptography` library maintainers
- All ethical hackers who educate responsibly

---

<div align="center">
  <strong>🔐 Learn security. Build defense. Never attack without permission.</strong>
</div>
```
