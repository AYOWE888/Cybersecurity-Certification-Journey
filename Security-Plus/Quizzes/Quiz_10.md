# 🛡️ CompTIA Security+ SY0-701: Encrypting Data (Domain 1.4)

## 📋 Executive Summary

Encryption protects data by converting it into unreadable ciphertext. It is categorized by the state of the data: **At Rest** (stored), **In Transit** (moving), or **In Process** (active).

---

## 🧱 Core Components

* **Data at Rest**: Inactive data on physical storage (SSDs/HDDs).
* **Data in Transit**: Information moving over a network (HTTPS, VPN).
* **Algorithm**: The public mathematical "lock" used to process data.
* **Key**: The secret "physical key" required to unlock the data.

---

## 🛠️ Encryption Solutions & States

| Solution | Scope | Platform | State | Logic |
| --- | --- | --- | --- | --- |
| **BitLocker** | Full Disk/Volume | Windows | At Rest | Encrypts the entire drive including OS |
| **FileVault** | Full Disk | macOS | At Rest | Native Mac startup disk protection |
| **EFS** | File/Folder | Windows | At Rest | Granular encryption within NTFS |
| **VPN** | Network Tunnel | Cross-Platform | In Transit | Creates an encrypted "pipe" for data |
| **TDE** | Database | SQL/Server | At Rest | Transparently encrypts the database file |

---

## ⚙️ Strength & Mitigation

* **Key Length**: Longer keys (e.g., 128-bit vs 256-bit) increase the "keyspace" to prevent Brute Force.
* **Key Stretching**: Running a hash/algorithm thousands of times (e.g., Argon2, bcrypt) to slow down attackers.
* **Symmetric vs Asymmetric**: Symmetric is fast (128/256 bits); Asymmetric is complex/related (3,072+ bits).

---

## 💡 Reflection on Core Concepts

**Q1: What is the primary difference between BitLocker and EFS?** BitLocker encrypts the entire volume/drive, while EFS provides granular encryption for specific files or folders.

**Q2: Why are encryption algorithms usually public rather than secret?** Public algorithms are vetted by the community for weaknesses; security relies entirely on the secrecy of the key, not the "math."

**Q3: How does "Key Stretching" protect weak passwords?** It forces the CPU to perform the encryption process multiple times, adding significant time overhead to every "guess" in a brute-force attack.

**Q4: What is "Transparent Encryption" in databases?** It automatically encrypts data when written to the disk and decrypts it when read, making the security invisible to the application.

---

## 📚 References & Resources

* Professor Messer – [Encrypting Data](https://www.google.com/search?q=https://youtu.be/jpsc4c7lntw)
* [CompTIA SY0-701 Exam Objectives](https://www.comptia.org)

---

🏆 **Proof of Completion (18/20)**
```
