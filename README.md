<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Ubuntu+Mono&size=13&duration=3000&pause=1000&color=E95420&center=true&width=600&lines=Initializing+kernel...;Loading+memory+manager...;Mounting+virtual+filesystem...;Starting+window+compositor...;SerenityOS+is+ready." alt="boot sequence"/>

```
██████╗ ███████╗
██╔═══██╗██╔════╝    P R I N C E K C H A U D H A R I / O S
██║   ██║███████╗    ─────────────────────────────────────
██║   ██║╚════██║    A complete operating system.
╚██████╔╝███████║    Written from scratch. No Linux. No UNIX.
 ╚═════╝ ╚══════╝    Just C++, Assembly, and raw ambition.
```

<img src="https://img.shields.io/badge/KERNEL-CUSTOM-purple?style=for-the-badge&labelColor=2b0a3d"/>
<img src="https://img.shields.io/badge/LANGUAGE-C%2B%2B23-E95420?style=for-the-badge&labelColor=1a1a1a"/>
<img src="https://img.shields.io/badge/LINES-1M%2B-77216F?style=for-the-badge&labelColor=1a1a1a"/>
<img src="https://img.shields.io/badge/ARCH-x86__64-white?style=for-the-badge&labelColor=1a1a1a"/>
<img src="https://img.shields.io/badge/LICENSE-BSD_2--Clause-E95420?style=for-the-badge&labelColor=1a1a1a"/>

</div>

---

<div align="center">

```
root@princekchaudhari:~# cat /etc/os-release
```

</div>

```yaml
NAME          : OS (SerenityOS)
VERSION       : rolling
AUTHOR        : PrinceKChaudhari
KERNEL        : custom monolithic
LANGUAGE      : C++23 + x86 Assembly
LINES_OF_CODE : 1,000,000+
ARCHITECTURE  : x86 / x86_64
EMULATOR      : QEMU
LICENSE       : BSD 2-Clause
STATUS        : active development
```

---

## `$ cat /proc/features`

```
[✔] Preemptive multitasking kernel
[✔] Virtual memory & paging
[✔] Custom VFS (Virtual Filesystem)
[✔] Native GUI — no X11, no Wayland
[✔] Custom web browser — no Chromium
[✔] TCP/IP networking stack from zero
[✔] Audio server & drivers
[✔] Custom LibC, LibGUI, LibCore, LibWeb
[✔] 1,000,000+ lines of pure C++
[✔] Runs in QEMU — boots in seconds
```

---

## `$ lsblk --tree`

```
OS/
├── Kernel/
│   ├── Arch/              # x86 boot, GDT, IDT, paging
│   ├── Memory/            # Virtual memory manager
│   ├── Process/           # Scheduler, threads, IPC
│   ├── FileSystem/        # VFS, ext2, tmpfs
│   └── Net/               # TCP/IP stack
│
├── Userland/
│   ├── Applications/
│   │   ├── Browser/       # Custom web browser
│   │   ├── Terminal/      # Shell & terminal emulator
│   │   ├── FileManager/   # GUI file manager
│   │   └── TextEditor/    # Built-in editor
│   ├── Libraries/
│   │   ├── LibC/          # Standard C library
│   │   ├── LibGUI/        # Widget toolkit
│   │   ├── LibCore/       # Core utilities
│   │   └── LibWeb/        # HTML/CSS engine
│   └── Services/
│       ├── WindowServer/  # Compositor
│       ├── AudioServer/   # Audio daemon
│       └── NetworkServer/ # Net daemon
│
├── Toolchain/             # Custom GCC cross-compiler
└── Meta/                  # Build scripts & CI
```

---

## `$ sudo apt install && make`

```bash
# ─── Step 1: Install dependencies ────────────────────────────
sudo apt install build-essential cmake ninja-build \
  libmpfr-dev libmpc-dev libgmp-dev \
  e2fsprogs qemu-system-i386 qemu-utils

# ─── Step 2: Clone ───────────────────────────────────────────
git clone https://github.com/PrinceKChaudhari/OS.git
cd OS

# ─── Step 3: Build toolchain (one time ~30 min) ──────────────
./Toolchain/BuildIt.sh

# ─── Step 4: Run ─────────────────────────────────────────────
./Meta/serenity.sh run
# Opens QEMU → full desktop OS boots
```

---

## `$ uname -a — Architecture`

```
┌─────────────────────────────────────────────────────┐
│                   APPLICATIONS                      │
│   Browser  ·  Terminal  ·  FileManager  ·  Editor   │
├─────────────────────────────────────────────────────┤
│              LIBRARIES & SERVICES                   │
│     LibC  ·  LibGUI  ·  LibWeb  ·  LibCore          │
├─────────────────────────────────────────────────────┤
│                    KERNEL                           │
│   Scheduler · Memory · VFS · Network · IPC          │
├─────────────────────────────────────────────────────┤
│              HARDWARE ABSTRACTION                   │
│        x86  ·  Drivers  ·  BIOS / UEFI              │
└─────────────────────────────────────────────────────┘
```

---

## `$ git contribute`

```bash
# Fork → Clone → Branch → PR

git clone https://github.com/PrinceKChaudhari/OS.git
git checkout -b fix/my-improvement
git commit -m "fix: describe your change"
git push origin fix/my-improvement
# Open Pull Request on GitHub
```

Good first issues are tagged `[GOOD FIRST BUG]` — contributions welcome.

---

## `$ man philosophy`

> Most hobby OS projects stop at a bootloader.
>
> This one has a browser, an audio server, a compositor,
> a custom LibC, and over one million lines of C++.
>
> *"An OS is not just software. It is a statement."*

---

<div align="center">

```
root@princekchaudhari:~# shutdown -h now
[ 0.000] Unmounting filesystems...
[ 0.012] Stopping services...
[ 0.024] See you next boot. 👋
```

<br/>

<img src="https://img.shields.io/badge/BUILT_BY-PrinceKChaudhari-77216F?style=for-the-badge&labelColor=2b0a3d"/>
<img src="https://img.shields.io/badge/⭐_STAR_THIS_REPO-E95420?style=for-the-badge"/>

<br/><br/>

![visitors](https://visitor-badge.laobi.icu/badge?page_id=PrinceKChaudhari.OS&left_color=2b0a3d&right_color=E95420)

</div>
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
