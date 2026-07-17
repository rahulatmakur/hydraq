# HyDraQ
### Hybrid Dual-Layer Adaptive Quantum Cryptographic Framework

> **An adaptive post-quantum file encryption framework designed to protect digital assets against both classical and future quantum computing threats.**

---

## Overview

HyDraQ is a cross-platform post-quantum file encryption framework developed as a Bachelor's capstone project in Cybersecurity. It combines NIST-standardized post-quantum cryptographic algorithms with an intelligent adaptive orchestration engine to provide secure, efficient, and scalable file encryption.

Unlike traditional encryption tools that apply the same protection to every file, HyDraQ analyzes each file's characteristics and automatically selects an appropriate encryption strategy, balancing security and performance.

The framework integrates:

- **ML-KEM (CRYSTALS-Kyber/Kyber512)** for post-quantum key encapsulation
- **ML-DSA (CRYSTALS-Dilithium/Dilithium2)** for digital signatures
- **AES-256-GCM** for authenticated symmetric encryption
- **SHAKE-256** for deterministic block permutation

---

# Features

## Post-Quantum Cryptography

- ML-KEM (Kyber512) secure key encapsulation
- ML-DSA (Dilithium2) digital signatures
- AES-256-GCM authenticated encryption
- Quantum-resistant cryptographic architecture

---

## Adaptive Security

HyDraQ automatically evaluates:

- File entropy
- File size
- User-selected sensitivity

The framework dynamically determines:

- Encryption depth
- Processing strategy
- Recursive encryption layers

without requiring manual configuration.

---

## Self-Describing Encryption

Each encrypted file securely stores:

- Encryption metadata
- Algorithm identifiers
- Required decryption parameters
- Integrity information

The metadata is digitally signed to detect tampering.

---

## Streaming Encryption

Large files are encrypted in chunks rather than loading the entire file into memory, providing:

- Lower memory consumption
- Improved scalability
- Faster processing
- Support for very large files

---

## Recursive Multi-Layer Encryption

HyDraQ supports recursive encryption where every layer uses:

- Independent AES session keys
- Independent ML-KEM encapsulation
- Independent integrity verification

---

## Cross-Platform

HyDraQ binaries are compatible with:

- Windows
- Linux
- macOS

No installation is required beyond the necessary runtime dependencies.

---

# Architecture

```
                 Input File
                      │
                      ▼
          Shannon Entropy Analysis
                      │
                      ▼
     Adaptive Orchestration Engine
                      │
          ┌───────────┴───────────┐
          │                       │
          ▼                       ▼
   AES Session Key        Metadata Generation
          │
          ▼
  ML-KEM Key Encapsulation
          │
          ▼
 SHAKE-256 Block Permutation
          │
          ▼
     AES-256-GCM Encryption
          │
          ▼
  ML-DSA Digital Signature
          │
          ▼
      Encrypted Output
```

---

# Technology Stack

| Category | Technology |
|----------|------------|
| Language | Python |
| Post-Quantum KEM | ML-KEM (Kyber512) |
| Digital Signatures | ML-DSA (Dilithium2) |
| Symmetric Encryption | AES-256-GCM |
| Hash Functions | SHA-256, SHAKE-256 |
| PQC Library | Open Quantum Safe (liboqs) |
| Packaging | Nuitka |

---

# Repository Contents

```
HyDraQ/
│
├── HyDraQ                # Executable binary
├── README.md
├── LICENSE
├── docs/
│   ├── Project_Report.pdf
│   ├── Architecture.pdf
│   └── User_Guide.pdf
└── screenshots/
```

---

# Usage

### Generate Keys

```
HyDraQ keygen
```

---

### Encrypt a File

```
HyDraQ encrypt <input_file> <output_file>
```

---

### Decrypt a File

```
HyDraQ decrypt <encrypted_file> <output_file>
```

---

# Security Features

- Post-quantum key encapsulation
- Post-quantum digital signatures
- Authenticated encryption
- Automatic parameter selection
- Adaptive encryption depth
- Tamper detection
- Secure metadata protection
- Streaming encryption
- Recursive encryption
- Cross-platform compatibility

---

# Applications

HyDraQ can be used for protecting:

- Confidential documents
- Government records
- Healthcare data
- Financial information
- Research datasets
- Long-term digital archives
- Enterprise backups

---

# Performance

HyDraQ improves efficiency through:

- Chunk-based file processing
- Streaming encryption
- SHAKE-256 block permutation
- Optimized recursive encryption pipeline
- Reduced memory usage

---

# Future Enhancements

- Graphical User Interface (GUI)
- Hardware acceleration
- Secure cloud integration
- Batch directory encryption
- Secure key management
- REST API
- Multi-user support
- Performance benchmarking dashboard

---

# Disclaimer

HyDraQ is an academic and research project developed as part of a Bachelor of Computer Applications (Cybersecurity) capstone project.

The framework implements standardized post-quantum cryptographic primitives (ML-KEM and ML-DSA) together with a custom adaptive orchestration framework. While extensive functional testing has been performed, the project has not undergone an independent professional cryptographic security audit and should not be considered a production-ready enterprise encryption solution.

---

# Source Code

This repository contains **compiled binaries and project documentation only**.

The source code is **not publicly available**.

---

# Author

**Rahul Aathmakur**

Bachelor of Computer Applications (Cybersecurity)

Lovely Professional University

---

# Acknowledgements

- NIST Post-Quantum Cryptography Standardization Project
- Open Quantum Safe (liboqs)
- Python Cryptography Community
- Lovely Professional University

---

# License

Copyright © 2026 Rahul Aathmakur.

All Rights Reserved.

This repository is provided for demonstration and evaluation purposes only. Redistribution, modification, reverse engineering, or commercial use of the binaries without prior written permission is prohibited.
