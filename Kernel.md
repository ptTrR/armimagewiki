---
title: Instruction
description: 
published: 1
date: 2021-01-03T03:52:46.808Z
tags: 
editor: undefined
dateCreated: 2020-12-21T09:11:32.322Z
---

## Linux Kernel for Debian, Devuan and Ubuntu

### Config Menu

```sh
Defconfig:    # Name of 'nameofdefconfig'_defconfig
Branch:       # Kernel branch
Arch:         # Supoported: x86, arm64 and arm (native compile only)
Menuconfig:   # 1 to run kernel menuconfig | 0 to skip
rtl88XXau:    # 1 to add Realtek 8812AU/14AU/21AU wireless support
rtl88XXbu:    # 1 to add Realtek 88X2BU wireless support
rtl88XXcu:    # 1 to add Realtek 8811CU/21CU wireless support
```
### Commands

```sh
make depends  # Install dependencies
make config   # Create a userdata.txt file
make kernel   # Build deb package
make purge    # Remove temporary directory
```
### User Patches

```sh
Patches "-p1" placed in the patches directory are applied during compilation.
```

### Notes

```sh
The name of your defconfig, will become the name of the kernel packages created.
For example: nameofdefconfig-linux-image nameofdefconfig-linux-headers
```