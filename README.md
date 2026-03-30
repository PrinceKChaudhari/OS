<div align="center">

[![Header](https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=200&section=header&text=OS%20Project&fontSize=60&fontColor=ffffff&animation=fadeIn&fontAlignY=40&desc=A%20complete%20operating%20system%20built%20from%20scratch&descSize=16&descAlignY=60&descColor=a0a0ff)](https://github.com/PrinceKChaudhari)

![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white&labelColor=0d1117)
![Assembly](https://img.shields.io/badge/Assembly-6E4C13?style=flat&logo=assemblyscript&logoColor=white&labelColor=0d1117)
![Lines of Code](https://img.shields.io/badge/Lines_of_Code-1M+-ff006e?style=flat&labelColor=0d1117)
![License](https://img.shields.io/badge/License-BSD_2--Clause-00d4ff?style=flat&labelColor=0d1117)
![Status](https://img.shields.io/badge/Status-Active-00ff41?style=flat&labelColor=0d1117)

### 💀 A fully custom operating system — kernel, GUI, browser, and everything in between.

</div>

---

## 🧠 What Is This?

This is a **complete, from-scratch operating system** written in C++ and x86 Assembly.

Not a Linux fork. Not a UNIX clone. A completely original OS with:

- 🖥️ **Custom Kernel** — memory management, scheduling, syscalls
- 🎨 **Native GUI** — window manager, compositor, widgets
- 🌐 **Custom Web Browser** — built from scratch, no Chromium
- 📁 **Custom Filesystem** — original VFS implementation
- 🔊 **Audio Stack** — custom audio server
- 🌍 **Networking** — TCP/IP stack written from zero
- 🧩 **1M+ lines of code** — one of the largest indie OS projects

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────┐
│             Applications                │
│  Browser · FileManager · Terminal · ... │
├─────────────────────────────────────────┤
│           LibC / LibCore / LibGUI        │
├─────────────────────────────────────────┤
│              Kernel                     │
│  Scheduler · MM · VFS · Net · IPC       │
├─────────────────────────────────────────┤
│         Hardware Abstraction            │
│      x86 · Drivers · BIOS/UEFI         │
└─────────────────────────────────────────┘
```

---

## 🚀 Build & Run

```bash
# Install dependencies (Ubuntu/Debian)
sudo apt install build-essential cmake ninja-build libmpfr-dev \
  libmpc-dev libgmp-dev e2fsprogs qemu-system-i386 qemu-utils

# Clone
git clone https://github.com/PrinceKChaudhari/OS.git
cd OS

# Build toolchain (one time)
./Toolchain/BuildIt.sh

# Build & run in QEMU
./Meta/serenity.sh run
```

---

## 📂 Project Structure

```
OS/
├── Kernel/          # Core kernel code
├── Userland/        # Userspace apps & libs
│   ├── Applications/  # Browser, terminal, etc
│   ├── Libraries/     # LibC, LibGUI, LibCore
│   └── Services/      # Audio, network daemons
├── Toolchain/       # Custom GCC toolchain
├── Meta/            # Build scripts
└── Documentation/   # Internals docs
```

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| Language | C++23, x86 Assembly |
| Build System | CMake + Ninja |
| Emulator | QEMU |
| Toolchain | Custom GCC cross-compiler |
| GUI | Custom compositor (no X11) |
| Browser | Custom (no Chromium/WebKit) |

---

## 🤝 Contributing

Pull requests welcome! Check open issues for good first contributions.

```bash
git checkout -b feature/my-feature
git commit -m "✨ add my feature"
git push origin feature/my-feature
```

---

<div align="center">

**⭐ Star this repo if you think building an OS from scratch is insane ⭐**

Made with 🤍 by [PrinceKChaudhari](https://github.com/PrinceKChaudhari)

[![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=120&section=footer)](https://github.com/PrinceKChaudhari)

</div>
