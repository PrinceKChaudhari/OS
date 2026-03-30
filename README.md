<!-- ============================================================
     OS — README
     by PrinceKChaudhari
     ============================================================ -->

<div align="center">

<!-- TOP ACCENT LINE -->
<img src="https://capsule-render.vercel.app/api?type=rect&color=0:ff3b30,100:ff3b30&height=4&section=header&reversal=false" width="100%"/>

<br/>

<!-- macOS WINDOW CHROME -->
<table>
<tr>
<td align="left" width="80px">&nbsp;&nbsp;🔴 🟡 🟢</td>
<td align="center"><sub><b>PrinceKChaudhari/OS — bash — 80×24</b></sub></td>
<td align="right" width="80px">&nbsp;</td>
</tr>
</table>

<!-- BIG ASCII LOGO -->
```
 ██████╗ ███████╗
██╔═══██╗██╔════╝
██║   ██║███████╗
██║   ██║╚════██║
╚██████╔╝███████║
 ╚═════╝ ╚══════╝
```

<!-- BOOT ANIMATION -->
<img src="https://readme-typing-svg.demolab.com?font=Ubuntu+Mono&size=14&duration=2000&pause=800&color=FF3B30&center=true&width=500&lines=%5B+OK+%5D+Starting+memory+manager...;%5B+OK+%5D+Mounting+virtual+filesystem...;%5B+OK+%5D+Loading+window+compositor...;%5B+OK+%5D+Starting+network+services...;%5B+OK+%5D+SerenityOS+ready.+Welcome%2C+Prince."/>

<br/><br/>

<!-- BADGE ROW -->
<img src="https://img.shields.io/badge/-C%2B%2B%2023-black?style=flat-square&logo=cplusplus&logoColor=FF3B30"/>
<img src="https://img.shields.io/badge/-x86__64-black?style=flat-square&logo=intel&logoColor=white"/>
<img src="https://img.shields.io/badge/-1M%2B%20Lines-black?style=flat-square&logoColor=FF3B30&color=111111&labelColor=FF3B30&label=CODE"/>
<img src="https://img.shields.io/badge/-No%20Linux-black?style=flat-square&color=111111"/>
<img src="https://img.shields.io/badge/-No%20UNIX-black?style=flat-square&color=111111"/>
<img src="https://img.shields.io/badge/-BSD%202--Clause-black?style=flat-square&color=FF3B30"/>

</div>

<br/>

---

<br/>

<!-- MANIFESTO — SPLIT LAYOUT -->
<table>
<tr>
<td width="50%" valign="top">

### What this is.

A complete operating system.
Built from scratch.
By one person.

A kernel. A window manager.  
A web browser. A filesystem.  
A TCP/IP stack. An audio server.  
A C standard library.

**Over one million lines of C++.**

Not a project. Not a tutorial.  
A statement.

</td>
<td width="50%" valign="top">

### What this is not.

<br/>

❌ &nbsp; Not a fork of Linux  
❌ &nbsp; Not a fork of UNIX  
❌ &nbsp; Not based on any existing kernel  
❌ &nbsp; Not a bootloader experiment  
❌ &nbsp; Not abandoned  

<br/>

✅ &nbsp; Written from absolute zero  
✅ &nbsp; Boots. Runs. Has a browser.  

</td>
</tr>
</table>

<br/>

---

<br/>

<!-- PULL QUOTE -->
<div align="center">

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:111111,100:111111&height=1" width="60%"/>

<br/><br/>

> <h3><i>"Most hobby OS projects stop at a bootloader.<br/>This one has a browser."</i></h3>

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:111111,100:111111&height=1" width="60%"/>

<br/>

</div>

<br/>

---

<br/>

<!-- SYSTEM INFO — htop style -->

### <kbd>F2</kbd> &nbsp; System Snapshot

<br/>

```
  COMPONENT           TECHNOLOGY              STATUS
  ─────────────────────────────────────────────────────────
  Kernel              Monolithic C++23        ████████████  running
  Scheduler           Preemptive, SMP         ████████████  running
  Memory Manager      Virtual + Paging        ████████████  running
  Virtual Filesystem  Custom VFS              ████████████  running
  Window Compositor   Software Rendering      ████████████  running
  Web Browser         LibWeb (no Chromium)    ████████████  running
  Audio Server        Custom daemon           ████████████  running
  TCP/IP Stack        Written from zero       ████████████  running
  LibC                Custom stdlib           ████████████  running
  Toolchain           Custom GCC cross        ████████████  running
  ─────────────────────────────────────────────────────────
  Total lines of code                         1,000,000+
```

<br/>

---

<br/>

<!-- ARCHITECTURE -->

### <kbd>F3</kbd> &nbsp; Architecture

<br/>

```
  ┌──────────────────────────────────────────────────────────┐
  │                                                          │
  │   ┌────────────┐  ┌──────────┐  ┌──────────────────┐   │
  │   │  Browser   │  │ Terminal │  │   File Manager   │   │
  │   └────────────┘  └──────────┘  └──────────────────┘   │
  │                    APPLICATIONS                          │
  ├──────────────────────────────────────────────────────────┤
  │                                                          │
  │     LibC    ·    LibGUI    ·    LibWeb    ·   LibCore    │
  │                    LIBRARIES                             │
  ├──────────────────────────────────────────────────────────┤
  │                                                          │
  │   WindowServer  ·  AudioServer  ·  NetworkServer        │
  │                    SERVICES                              │
  ├──────────────────────────────────────────────────────────┤
  │                                                          │
  │   Scheduler  ·  Memory  ·  VFS  ·  Net  ·  IPC  · IRQ  │
  │                     KERNEL                               │
  ├──────────────────────────────────────────────────────────┤
  │                                                          │
  │            x86 Drivers  ·  BIOS/UEFI  ·  QEMU           │
  │                    HARDWARE                              │
  └──────────────────────────────────────────────────────────┘
```

<br/>

---

<br/>

<!-- FILE TREE -->

### <kbd>F4</kbd> &nbsp; Structure

<br/>

<details>
<summary><b>Click to expand full tree</b></summary>

<br/>

```
OS/
│
├── Kernel/
│   ├── Arch/x86/              ← boot, GDT, IDT, paging
│   ├── Devices/               ← block, char, net drivers
│   ├── FileSystem/            ← VFS, ext2, procfs, tmpfs
│   ├── Memory/                ← VMM, kmalloc, regions
│   ├── Net/                   ← TCP, UDP, IP, ARP, DNS
│   └── Process/               ← scheduler, threads, IPC
│
├── Userland/
│   ├── Applications/
│   │   ├── Browser/           ← full web browser
│   │   ├── Terminal/          ← shell + terminal emulator
│   │   ├── FileManager/       ← GUI file manager
│   │   └── TextEditor/        ← built-in editor
│   │
│   ├── Libraries/
│   │   ├── LibC/              ← C standard library
│   │   ├── LibGUI/            ← widget toolkit
│   │   ├── LibCore/           ← core utilities
│   │   └── LibWeb/            ← HTML/CSS/JS engine
│   │
│   └── Services/
│       ├── WindowServer/      ← compositor + WM
│       ├── AudioServer/       ← audio daemon
│       └── NetworkServer/     ← network daemon
│
├── Toolchain/                 ← custom GCC cross-compiler
└── Meta/                      ← build system + CI scripts
```

</details>

<br/>

---

<br/>

<!-- BUILD INSTRUCTIONS -->

### <kbd>F5</kbd> &nbsp; Build & Run

<br/>

```bash
# ── 1. Install dependencies ────────────────────────────────
sudo apt install build-essential cmake ninja-build      \
  libmpfr-dev libmpc-dev libgmp-dev                     \
  e2fsprogs qemu-system-i386 qemu-utils

# ── 2. Clone ───────────────────────────────────────────────
git clone https://github.com/PrinceKChaudhari/OS.git
cd OS

# ── 3. Build toolchain (one time, ~30 min) ─────────────────
./Toolchain/BuildIt.sh

# ── 4. Build + launch ──────────────────────────────────────
./Meta/serenity.sh run
# → QEMU launches → full GUI desktop boots
```

<br/>

> [!NOTE]
> First build takes ~30 minutes (compiling custom GCC toolchain).
> Subsequent builds are fast — only changed files recompile.

<br/>

---

<br/>

<!-- CONTRIBUTE -->

### <kbd>F6</kbd> &nbsp; Contribute

<br/>

<table>
<tr>
<td valign="top" width="50%">

Good first issues are tagged  
<kbd>good first bug</kbd>

All contributions welcome —  
bug fixes, drivers, apps, docs.

</td>
<td valign="top" width="50%">

```bash
git checkout -b fix/issue-name
# make your changes
git commit -m "fix: description"
git push origin fix/issue-name
# open PR on GitHub
```

</td>
</tr>
</table>

<br/>

---

<br/>

<!-- CLOSING -->

<div align="center">

<br/>

```
[ 0.000 ] Unmounting filesystems...
[ 0.012 ] Flushing disk cache...
[ 0.019 ] Stopping all services...
[ 0.031 ] Goodbye.
```

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:ff3b30,100:ff3b30&height=4&section=footer" width="100%"/>

<br/>

<sub>Built with obsession by <a href="https://github.com/PrinceKChaudhari"><b>PrinceKChaudhari</b></a> &nbsp;·&nbsp; BSD 2-Clause License</sub>

<br/>

![visitors](https://visitor-badge.laobi.icu/badge?page_id=PrinceKChaudhari.OS&left_color=111111&right_color=FF3B30&left_text=visitors)

<br/>

</div>
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
