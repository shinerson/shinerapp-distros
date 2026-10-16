# SHINER Application Distributions

Public downloads for the SHINER application.

Current public release: **SHINER 0.9.7a2 (ALPHA)**.

These packages passed automated packaging and content verification. Native
recipient installation, upgrade and uninstall UAT remains pending.

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
