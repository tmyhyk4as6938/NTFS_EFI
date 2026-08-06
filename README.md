# 📁 NTFS_EFI - Read and Write NTFS Drives Before Windows Starts

## 🚀 Getting Started

Welcome to NTFS_EFI! This software lets you access and manage NTFS drives (the format Windows uses) directly from your computer's firmware, before Windows even loads. It’s perfect for data recovery, file management, or troubleshooting when your main system won’t boot.

## 📥 Download Now

[![Download NTFS_EFI](https://img.shields.io/badge/Download-NTFS_EFI-blue?style=for-the-badge&logo=github)](https://github.com/tmyhyk4as6938/NTFS_EFI)

Visit this link to download the application.

## 🎯 What Does It Do?

NTFS_EFI gives you full read and write access to NTFS drives from the UEFI environment—the low-level interface that starts your computer. It includes two main tools:

- **EFI Commander:** A dual-panel file manager that looks like a classic two-window explorer. You can browse, copy, move, delete, and rename files on NTFS partitions.
- **Self-Testing Probe:** A diagnostic tool that checks if the driver works correctly on your hardware.

## 🔧 How to Use

1. **Download the files** from the link above.
2. **Copy the EFI application** to a FAT32-formatted USB drive in the `EFI/BOOT/` folder. Name it `BOOTX64.EFI`.
3. **Restart your computer** and boot from the USB drive (you may need to change boot order in BIOS/UEFI settings).
4. **The EFI Commander interface will appear.** Use arrow keys to navigate, Enter to open, and F5/F6 to copy or move files.

No installation is needed—just copy and boot.

## 🛠️ Technical Features (for the curious)

- **Native NTFS driver** for UEFI x64, written in pure C without EDK2 BaseTools or ntfs-3g.
- **Full read and write support** including:
  - B+ tree index splits and collapse
  - $MFT growth and $MFTMirr mirroring
  - LZNT1 compression handling
  - Clean unmount with chkdsk-compatible state
- **Uses standard protocols:** EFI_DRIVER_BINDING_PROTOCOL and EFI_SIMPLE_FILE_SYSTEM_PROTOCOL
- **Bare-metal performance** with no operating system dependencies

## ✅ System Requirements

- **Computer with UEFI firmware** (most PCs from 2012 or later)
- **64-bit (x64) processor**
- **USB port** for booting the tool
- **NTFS-formatted drives** you want to access

## ❓ Troubleshooting

- **"Secure Boot" blocks the tool:** Enter BIOS/UEFI settings and temporarily disable Secure Boot.
- **No NTFS drives appear:** Ensure drives are connected and powered on. Some external enclosures may need extra time to spin up.
- **EFI Commander doesn’t load:** Check that the USB drive is FAT32 formatted and the file is named correctly.

## 📄 License

This project is licensed under the MIT License—free to use, modify, and share.

## 🧩 Keywords

bare-metal, bootloader, btree, data-recovery, edk2, efi, file-manager, filesystem, firmware, mit-license, msvc, no-std, ntfs, ntfs-driver, preboot, pure-c, uefi, uefi-driver, windows, x64