# 2-TEK Ecosystem — VTek Development Suite (Official Downloads & Distribution Center)

> **Official Binary Release Directory Structure**:
> All desktop application packages and release distributions are compiled and published using the canonical app-scoped versioned structure:
> **`{suitRoot}/{app}/{version}/{name}.{type}`**
> _(Thư mục phân phối chính thức toàn bộ bộ cài đặt desktop và standalone packages cho các ứng dụng hệ sinh thái 2-TEK Development Suite: LocalSQLServer, LocalVectorServer / LowcodeVectorDB, LocalSQLClient, LocalVectorClient, LowcodeServer)_.
>
> 🎯 **Canonical Target**:
> Dedicated repository strictly used for displaying public binary packages and installers of 2tek-development-packs: zero source code, zero scripts, no package.json, pure distribution binaries and metadata.
>
> 🔗 **Standalone Git Repository — [github.com/vietcoder1998/DevelopmentSuit](https://github.com/vietcoder1998/DevelopmentSuit)**:
> This is an independent, dedicated public project distribution repository (lives at `~/Projects/VtekDevelopmentSuit`) matching the distribution architecture of VTekOfficeSuit.

---

## 1. Directory Structure Standard

```
DevelopmentSuit/  (~https://github.com/vietcoder1998/DevelopmentSuit)
├── .git/                                 # Dedicated distribution Git repository
├── README.md                             # Official release center documentation
├── LICENSE                               # MIT License
├── .gitignore                            # Distribution repository ignore rules
├── LocalSQLServer/                       # LocalSQLServer database engine
│   └── 1.0.2/
│       ├── LocalSQLServer-1.0.2.deb      # Linux Debian package (amd64)
│       ├── LocalSQLServer-1.0.2.exe      # Windows PE32+ GUI installer (x64)
│       ├── LocalSQLServer-1.0.2.dmg      # macOS Apple Disk Image (universal)
│       ├── LocalSQLServer-1.0.2.zip      # Universal portable application bundle
│       ├── SHA256SUMS.txt                # SHA-256 verification checksums
│       └── release-manifest.json         # Automated release metadata
├── LocalVectorServer/                     # LocalVectorServer / LowcodeVectorDB engine
│   └── 1.0.2/
│       ├── LocalVectorServer-1.0.2.deb
│       ├── LocalVectorServer-1.0.2.exe
│       ├── LocalVectorServer-1.0.2.dmg
│       ├── LocalVectorServer-1.0.2.zip
│       ├── SHA256SUMS.txt
│       └── release-manifest.json
├── LocalDBClient/                        # LocalDBClient unified database studio
│   └── 1.0.0/
│       ├── LocalDBClient-1.0.0.deb
│       ├── LocalDBClient-1.0.0.exe
│       ├── LocalDBClient-1.0.0.dmg
│       ├── LocalDBClient-1.0.0.zip
│       ├── SHA256SUMS.txt
│       └── release-manifest.json
└── LowcodeServer/                        # LowcodeServer application generation backend
    └── 1.0.0/
        ├── LowcodeServer-1.0.0.deb
        ├── LowcodeServer-1.0.0.exe
        ├── LowcodeServer-1.0.0.dmg
        ├── LowcodeServer-1.0.0.zip
        ├── SHA256SUMS.txt
        └── release-manifest.json
```

---

## 2. Included Applications

| Application | Canonical Role | Default Port | gRPC Port | Packages Available |
| ----------- | -------------- | ------------ | --------- | ------------------ |
| **LocalSQLServer** | High-performance local SQL database engine with HTTP REST and gRPC | `3110` | `50055` | `.deb`, `.exe`, `.dmg`, `.zip` |
| **LocalVectorServer** _(LowcodeVectorDB)_ | Vector database server for conversation search, knowledge base indexing & AI model training | `3120` | `50056` | `.deb`, `.exe`, `.dmg`, `.zip` |
| **LocalDBClient** | Unified database studio connecting SQL & Vector servers via HTTP, gRPC, WebSocket & IPC | `3033` | — | `.deb`, `.exe`, `.dmg`, `.zip` |
| **LowcodeServer** | Fullstack app generator service for LowcodeStudio | `3035` | `50057` | `.deb`, `.exe`, `.dmg`, `.zip` |

---

## 3. Installation & Setup Instructions

### 3.1. Linux (.deb)
```bash
sudo dpkg -i LocalSQLServer-1.0.2.deb
# Or for vector database:
sudo dpkg -i LocalVectorServer-1.0.2.deb
```

### 3.2. Windows (.exe)
Run the PE32+ executable installer:
```powershell
.\LocalSQLServer-1.0.2.exe
```

### 3.3. macOS (.dmg)
Mount the Apple Disk Image and drag the application to `/Applications`:
```bash
hdiutil attach LocalSQLServer-1.0.2.dmg
```

### 3.4. Universal Portable (.zip)
Extract and launch directly with Node.js:
```bash
unzip LocalSQLServer-1.0.2.zip -d LocalSQLServer
cd LocalSQLServer
node server.js
```

---

## 4. Integrity Verification

Every release includes `SHA256SUMS.txt` to verify binary integrity:
```bash
sha256sum -c SHA256SUMS.txt
```

---

## License
MIT License — Copyright (c) 2026 2-TEK Team.
# DevelopmentSuit
