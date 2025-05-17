# Kali Secure USB Builder — Hardened & Persistent Kali Live on Any Drive

🛠️ Create a secure, persistent and bootable Kali Linux environment (USB or NVMe) with custom GRUB — in just 2 scripts.

## Features

- 🔐 Hardened disk layout (FAT32 + EXT4 with / union)
- 💾 Real persistence partition (not overlay)
- 🧱 Prepares, formats and names partitions cleanly
- 📦 Copies Kali ISO content to bootable FAT32
- ⚙️ Installs GRUB BIOS (i386-pc) bootloader
- 🧩 Generates a working grub.cfg with persistence enabled

## Usage

```bash
git clone https://github.com/filouzzz/kali-secure-usb-builder
cd kali-secure-usb-builder
sudo ./1_prepare_disk.sh
sudo ./2_install_kali_grub_interactive.sh
```

## Requirements

- 🧪 A Kali ISO file downloaded locally
- 💽 A USB or NVMe target disk (everything will be wiped)
- 🧰 Tools installed: `parted`, `mkfs.vfat`, `mkfs.ext4`, `mount`, `umount`, `rsync`, `grub-install`

## 📚 Use Cases & Limitations

### ✅ What this project handles
- Create a bootable Kali Live system with persistence on any USB or NVMe disk
- Use the same disk on different machines, even via USB-C enclosures
- Fully re-installable via two clean scripts
- Ready for image-based deployment (e.g. .img.gz.gpg)

### ❌ What this script does NOT do (yet)
- UEFI boot support (BIOS-only for now)
- Dynamic hardware detection or tuning
- Automatic environment hardening (UFW, sudo, services… planned)
- Dual boot or multi-ISO support (can be added manually)

## Author

**filouzzz** – real-world driven Linux user and zero-trust enthusiast ⚔️
