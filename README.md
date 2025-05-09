
# Prince-Ransomware (🛡️ For Educational & Research Use Only)

> 🚨 This project is intended strictly for **educational and ethical security research purposes**.  
> **Do not deploy** or distribute this tool in any real-world environment without permission.  
> Misuse may be illegal and is not supported or endorsed by the author.

---

## 📌 About

**Prince-Ransomware** is a **simulated ransomware** tool built in Go, designed to demonstrate how modern ransomware operates — including hybrid encryption, file targeting, and key generation.

This project serves as a learning resource for:
- Cybersecurity researchers
- Malware analysts
- Ethical hackers
- Students studying encryption or malware behavior

---

## ⚙️ Features

- 🔐 **ChaCha20** stream cipher for fast symmetric encryption
- 🔑 **Elliptic Curve (ECIES)** public-key encryption for secure key wrapping
- 📁 Selective directory targeting (avoids critical system paths)
- 📄 File renaming with `.prince` extension
- 🗝️ Key pair generation via a builder tool
- 🔓 Decryptor included to restore encrypted files (requires private key)
- ⚙️ Compatible with Linux & Windows (tested with Go 1.21+)

---

## 🛠️ Project Structure

```
Prince-Ransomware/
├── Builder/       # Builds a ransomware encryptor with embedded public key
├── Encryptor/     # The actual ransomware binary that encrypts files
├── Decryptor/     # Tool to decrypt previously encrypted files
├── LICENSE
└── README.md
```

---

## 🚀 How to Use (Sandbox Only)

### 1. Build the Builder Tool

```bash
cd Builder
go build -o builder
./builder
```

This generates:
- `Encryptor` binary (the simulated ransomware)
- `Decryptor` binary
- Key pair (public & private)

---

### 2. Run the Encryptor

> ⚠️ Only run inside a **virtual machine or Docker container** with access to **test files only**.

```bash
cd Encryptor
./Encryptor
```

Your test files will be encrypted and renamed with `.prince`.

---

### 3. Run the Decryptor

```bash
cd ../Decryptor
./Decryptor
```

You’ll need the corresponding private key to decrypt files successfully.

---

## 🐳 Docker Sandbox Setup (Recommended)

Build a safe testing environment using Docker.  
See `sandbox-setup.md` for full instructions.

---

## ⚠️ Disclaimer

This project is provided for **educational purposes only**.

- 💣 Do not deploy in production.
- 💀 Do not run on live machines.
- 🧑‍⚖️ The author takes **no responsibility** for misuse or data loss.

---

## 📚 Credits

- Cryptography: [Go standard libs + ECIES]
- Author: [Pruthvi]
- Inspired by real-world ransomware for educational simulation

---

## 📜 License

MIT License — see `LICENSE` for details.
