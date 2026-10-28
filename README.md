# SHINER Application Distributions

Public downloads for the SHINER application.

Current public release: **SHINER 0.9.7a2 (ALPHA)**.

These packages passed automated packaging and content verification. Native
recipient installation, upgrade and uninstall UAT remains pending.

## Current UAT candidate — 0.9.7a2 (Linux 2~rc2 and macOS ARM64)

**RC2 is the current UAT candidate. Native recipient installation, startup,
upgrade, removal, and user-data preservation UAT remains pending on all targets.**

[UAT prerelease v0.9.7a2-pkg2rc2](https://github.com/shinerson/shinerapp-distros/releases/tag/v0.9.7a2-pkg2rc2) contains:

| Target | Candidate | Checksum |
| --- | --- | --- |
| Ubuntu 26.04 LTS x86_64 | [Download](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2-pkg2rc2/SHINER-0.9.7a2-pkg2rc2-Ubuntu-26.04-x86_64.deb) | [SHA-256](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2-pkg2rc2/SHINER-0.9.7a2-pkg2rc2-Ubuntu-26.04-x86_64.deb.sha256) |
| Debian 13 amd64 | [Download](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2-pkg2rc2/SHINER-0.9.7a2-pkg2rc2-Debian-13-amd64.deb) | [SHA-256](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2-pkg2rc2/SHINER-0.9.7a2-pkg2rc2-Debian-13-amd64.deb.sha256) |
| Fedora 42 x86_64 | [Download](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2-pkg2rc2/SHINER-0.9.7a2-pkg2rc2-Fedora-42-x86_64.rpm) | [SHA-256](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2-pkg2rc2/SHINER-0.9.7a2-pkg2rc2-Fedora-42-x86_64.rpm.sha256) |
| macOS 15 Apple Silicon ARM64 | [Download DMG](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2-pkg2rc2/MoonSHINER-0.9.7a2-macOS-arm64-50ea41c215d0.dmg) | [SHA-256](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2-pkg2rc2/MoonSHINER-0.9.7a2-macOS-arm64-50ea41c215d0.dmg.sha256) |

Linux application source: `2c27f871a20a06bc40acbc953d4512e8e464d5ad`.
[Source Quality Gate #231 passed](https://github.com/shinerson/shiner-engineering-manager/actions/runs/40277826795).

RC2 includes the accepted Help/Platform Doctor menu mouse-restoration correction
(UI-MOUSE-01), safe non-graphical KiCad detection and bounded diagnostic probes
(DOCTOR-KICAD-01), and current application documentation. Application version
remains **0.9.7a2**. Ubuntu requires Python 3.14; Debian/Fedora require Python 3.13.

All three packages passed automated metadata, dependency, inventory, source/resource,
RECORD, checksum, desktop integration, and extracted-payload checks. Packaging,
mouse/Doctor, learning, and offline Help regressions passed. Extracted runtime
checks used host Python 3.14; native Debian/Fedora Python 3.13 execution remains
pending. See the [RC2 notes](release-notes/v0.9.7a2-pkg2rc2.md) for scope and UAT items.

Download the matching package and `.sha256` sidecar, then require
`sha256sum -c <package>.sha256` to report `OK` before testing. Substitute the RC2
filename in the applicable package-manager procedure below.

The public `v0.9.7a2` release and its installation instructions remain unchanged.
RC1 is retained during this publication for possible upgrade comparisons; any
retirement is a separate follow-up.

### macOS Apple Silicon ARM64 — UAT candidate

**Native macOS UAT status: PENDING.** The project owner must perform physical
Apple Silicon Mac installation and application Acceptance Testing. Automated
checks do not establish successful native human UAT.

- [Download MoonSHINER ARM64 DMG](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2-pkg2rc2/MoonSHINER-0.9.7a2-macOS-arm64-50ea41c215d0.dmg)
- [Download matching SHA-256 file](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2-pkg2rc2/MoonSHINER-0.9.7a2-macOS-arm64-50ea41c215d0.dmg.sha256)
- Exact macOS application source commit:
  [`50ea41c215d0d6c5332bc81b25b19a8d8fe98d30`](https://github.com/shinerson/shiner-engineering-manager/commit/50ea41c215d0d6c5332bc81b25b19a8d8fe98d30).
- Provenance: [macOS ARM64 UAT Candidate #4, run 40622127848](https://github.com/shinerson/shiner-engineering-manager/actions/runs/40622127848),
  with its [successful exact-commit Quality Gate](https://github.com/shinerson/shiner-engineering-manager/actions/runs/40622127894).
  The approved Actions DMG is published unchanged; it has not been rebuilt.
- Application version: **0.9.7a2**. This macOS asset is identified by its source
  commit; the **2~rc2 packaging revision applies to the existing Linux packages**.
- Initial target: **macOS 15, Apple Silicon ARM64**; built and checked on macOS
  15.7.9. Intel Macs and other macOS versions have not been validated.
  Python 3.12.10 and required runtime dependencies are bundled. Python, Xcode,
  Git and development tools are not required to start SHINER. KiCad and other
  optional engineering tools remain separate installations.

**Verify the download**

Save the DMG and its `.dmg.sha256` file together. In Terminal, change to that
folder and run:

```sh
shasum -a 256 -c MoonSHINER-0.9.7a2-macOS-arm64-50ea41c215d0.dmg.sha256
```

Require `OK`. Expected DMG SHA-256:

```text
1ec1cb471337db880777ff0ae92c3f62e6d92d41705b84f0d8df0669bde3be8b
```

**Install and start**

1. Open the verified DMG in Finder and drag `MoonSHINER.app` to Applications.
   A normal-user `~/Applications` folder is also suitable.
2. Eject the disk image and open the copied application as your normal user.
   It opens Apple's Terminal for interactive keyboard and mouse operation.
3. Enlarge Terminal to at least **140 columns by 35 rows**. Follow first-run
   setup, then use **[0] Exit** to quit. A completed Terminal window may remain
   open according to its profile; close that window yourself.

Projects remain outside the app bundle. The default first-run project location
is `~/Documents/shinerapp_projects`; other accessible folders and OS-mounted
storage remain supported. The canonical icon, Guided Tutorial and appendices,
Mentorials, offline HTML Help, Markdown export and example project are included.

**Unsigned application and Gatekeeper**

This candidate has local ad-hoc signatures only: **no Apple Developer ID signing
or notarization**. Gatekeeper may block its first launch.

After verifying the checksum and choosing to trust the candidate, try opening
the copied app. If blocked as an unidentified-developer or unnotarized app, open
**System Settings > Privacy & Security** and select **Open Anyway** for this app.
Confirm **Open** and authenticate if asked. This is a per-app exception. See
[Apple's supported procedure](https://support.apple.com/en-us/102445).

Keep Gatekeeper enabled and retain quarantine attributes; do not change global
security policy. If managed policy hides the exception, or macOS reports malware,
revocation, damage or tampering, stop and report the message.

**Remove and test**

Exit SHINER, close its completed Terminal window, and move only the copied
`MoonSHINER.app` to Trash. Keep external project folders, settings, logs and
exports. Removing the downloaded DMG is separate from removing the installed app.
No global Python installation or background service is added.

Native UAT remains **PENDING**: check Finder installation and startup, unsigned
app prompts, keyboard and mouse behavior, resizing, offline books/images,
Markdown export, a disposable example project, normal exit/Ctrl-C, removal and
user-data preservation. Terminal's **View > Allow Mouse Reporting** must permit
reporting for mouse tests. The app retains its existing mouse-policy negotiation.
[Detailed source-version UAT checklist](https://github.com/shinerson/shiner-engineering-manager/blob/50ea41c215d0d6c5332bc81b25b19a8d8fe98d30/docs/MACOS_ARM64.md).

## Choose your platform

### Ubuntu 26.04 x86_64

**SHINER 0.9.7a2 — Ubuntu 26.04 x86_64**

[**Download SHINER 0.9.7a2 for Ubuntu 26.04 (.deb)**](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2/SHINER-0.9.7a2-Ubuntu-26.04-x86_64.deb)

[SHA-256 checksum](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2/SHINER-0.9.7a2-Ubuntu-26.04-x86_64.deb.sha256)

Native Ubuntu package. Installs Moonshiner as an Ubuntu application and is
managed through Ubuntu's normal apt/dpkg package system.

### Debian 13 amd64

**SHINER 0.9.7a2 — Debian 13 amd64**

[**Download SHINER 0.9.7a2 for Debian 13 (.deb)**](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2/SHINER-0.9.7a2-Debian-13-amd64.deb)

[SHA-256 checksum](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2/SHINER-0.9.7a2-Debian-13-amd64.deb.sha256)

Native Debian package. Installs Moonshiner as a Debian application and is
managed through Debian's normal apt/dpkg package system.

### Fedora 42 x86_64

**SHINER 0.9.7a2 — Fedora 42 x86_64**

[Download SHINER 0.9.7a2 for Fedora 42 (.rpm)](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2/SHINER-0.9.7a2-Fedora-42-x86_64.rpm)

[SHA-256 checksum](https://github.com/shinerson/shinerapp-distros/releases/download/v0.9.7a2/SHINER-0.9.7a2-Fedora-42-x86_64.rpm.sha256)

Native Fedora package. Installs Moonshiner as a Fedora application and is managed through Fedora's normal dnf/rpm package system.

## Install, Start, Update, or Remove SHINER (v0.9.7a2)

SHINER v0.9.7a2 is an **ALPHA** release for the Linux systems below. Native installation, update, and removal tests on the target systems are still pending.

Use the package for your Linux distribution. Do not install an Ubuntu package on Debian, or a Debian package on Ubuntu.

### Before you start

1. Open a terminal.
2. Identify your Linux distribution:

   ```bash
   cat /etc/os-release
   ```

3. Check the processor architecture:

   ```bash
   uname -m
   ```

4. Make sure the result is `x86_64`. The Debian package uses the equivalent name `amd64`.
5. Open the [SHINER v0.9.7a2 release page](https://github.com/shinerson/shinerapp-distros/releases/tag/v0.9.7a2).
6. Download the package for your distribution. Also download its matching `.sha256` file.
7. Save both files in `~/Downloads`.

**Important:** The checksum must report `OK` before you install a package. If it does not, stop. Download both files again.

The commands below install local package files. They do not add a SHINER software repository. Your package manager can require an internet connection to install system dependencies. Ubuntu requires Python 3.14. Debian 13 and Fedora 42 require Python 3.13.

### Ubuntu 26.04 LTS

**Files to download**

- `SHINER-0.9.7a2-Ubuntu-26.04-x86_64.deb`
- `SHINER-0.9.7a2-Ubuntu-26.04-x86_64.deb.sha256`

**Check the download**

1. Open a terminal and go to `~/Downloads`:

   ```bash
   cd "$HOME/Downloads"
   ```

2. Check the package:

   ```bash
   sha256sum -c SHINER-0.9.7a2-Ubuntu-26.04-x86_64.deb.sha256
   ```

3. Continue only if the command reports `OK`.

**Install or update SHINER**

1. Run this command:

   ```bash
   sudo apt install ./SHINER-0.9.7a2-Ubuntu-26.04-x86_64.deb
   ```

2. Read the package manager's proposed changes. Confirm them to continue.
3. Check the installed package:

   ```bash
   dpkg-query -W shiner
   ```

4. Start SHINER as your normal user:

   ```bash
   mshiner
   ```

**Remove SHINER**

1. Close SHINER.
2. Run this command:

   ```bash
   sudo apt remove shiner
   ```

3. Read the proposed changes. Confirm them to continue.

### Debian 13

**Files to download**

- `SHINER-0.9.7a2-Debian-13-amd64.deb`
- `SHINER-0.9.7a2-Debian-13-amd64.deb.sha256`

**Check the download**

1. Open a terminal and go to `~/Downloads`:

   ```bash
   cd "$HOME/Downloads"
   ```

2. Check the package:

   ```bash
   sha256sum -c SHINER-0.9.7a2-Debian-13-amd64.deb.sha256
   ```

3. Continue only if the command reports `OK`.

**Install or update SHINER**

1. Run this command:

   ```bash
   sudo apt install ./SHINER-0.9.7a2-Debian-13-amd64.deb
   ```

2. Read the package manager's proposed changes. Confirm them to continue.
3. Check the installed package:

   ```bash
   dpkg-query -W shiner
   ```

4. Start SHINER as your normal user:

   ```bash
   mshiner
   ```

**Remove SHINER**

1. Close SHINER.
2. Run this command:

   ```bash
   sudo apt remove shiner
   ```

3. Read the proposed changes. Confirm them to continue.

### Fedora 42

**Files to download**

- `SHINER-0.9.7a2-Fedora-42-x86_64.rpm`
- `SHINER-0.9.7a2-Fedora-42-x86_64.rpm.sha256`

**Check the download**

1. Open a terminal and go to `~/Downloads`:

   ```bash
   cd "$HOME/Downloads"
   ```

2. Check the package:

   ```bash
   sha256sum -c SHINER-0.9.7a2-Fedora-42-x86_64.rpm.sha256
   ```

3. Continue only if the command reports `OK`.

**Install or update SHINER**

1. Run this command:

   ```bash
   sudo dnf install ./SHINER-0.9.7a2-Fedora-42-x86_64.rpm
   ```

2. Read the package manager's proposed changes. Confirm them to continue.
3. Check the installed package:

   ```bash
   rpm -q shiner
   ```

4. Start SHINER as your normal user:

   ```bash
   mshiner
   ```

**Remove SHINER**

1. Close SHINER.
2. Run this command:

   ```bash
   sudo dnf remove shiner
   ```

3. Read the proposed changes. Confirm them to continue.

### First start and project files

Start SHINER with `mshiner` or `shiner`. You can also use the Moonshiner desktop launcher.

**Do not use `sudo` to start SHINER.** Use `sudo` only for the package manager commands shown above.

SHINER opens Home with no active project. During the first start, the application can ask you to set up its user-owned project location. The default location is `~/Documents/shinerapp_projects`.

The package installer does not create your projects or user settings. The remove commands above remove the installed software package. They are **not** instructions to delete your engineering files.

Keep a backup of important work. Do not delete `~/Documents/shinerapp_projects` or your user settings when you remove SHINER. Preservation of user data during native removal has not yet been verified on each target system.

To install a later version, download the new package for your distribution. Check its `.sha256` file. Then use the applicable **Install or update SHINER** procedure above.

## About

`shinerapp-distros` is the authoritative public distribution repository for
SHINER.

Current native packages for supported platforms are published as release assets
in this repository. Older releases remain available as historical versions.

[Historical SHINER v0.9.7a1 release and assets](https://github.com/shinerson/shinerapp-distros/releases/tag/v0.9.7a1)
remain unchanged and available.

Platform-specific repositories from earlier SHINER distribution models are
retired and are not authoritative sources for current downloads.
