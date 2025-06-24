# ft_linux - How to Train Your Kernel

> Build a basic, but functional, Linux distribution from scratch

## 📋 Project Overview

This project involves building a complete Linux distribution from the ground up, including compiling the kernel, installing essential packages, and configuring the system.

## 🎯 Main Goals

- [ ] Build a Linux Kernel
- [ ] Install essential binaries (see package list below)
- [ ] Implement a filesystem hierarchy compliant with standards
- [ ] Connect to the Internet

## 📚 Resources

- **Linux From Scratch (LFS)** - The Bible for building Linux from scratch
- **Kernel Documentation** - Official Linux kernel documentation
- **GNU Autotools** - For building packages from source
- Online tutorials and step-by-step guides for custom kernel building

## ⚙️ System Requirements

### Prerequisites

- [ ] Virtual Machine (VirtualBox, VMWare, or QEMU recommended)
- [ ] Host system with development tools
- [ ] Stable internet connection for downloading sources

### Technical Specifications

- [ ] **Kernel Version**: Must use Linux kernel 4.x (stable or development)
- [ ] **Architecture**: Choose between 32-bit or 64-bit system
- [ ] **Kernel Sources Location**: `/usr/src/kernel-$(version)`
- [ ] **Kernel Version Format**: `Linux kernel 4.x.x-<student_login>`
- [ ] **Hostname**: Set to your student login
- [ ] **Kernel Binary**: `/boot/vmlinuz-<linux_version>-<student_login>`

### Partitioning Requirements

- [ ] **Root partition** (/)
- [ ] **Boot partition** (/boot)
- [ ] **Swap partition**
- [ ] Additional partitions (optional but recommended)

### System Components

- [ ] **Kernel Module Loader**: udev or equivalent
- [ ] **Init System**: SysV or SystemD
- [ ] **Bootloader**: GRUB or LILO

## 🚀 Getting Started

### Phase 1: Environment Setup

- [ ] Set up virtual machine with adequate resources (4GB+ RAM, 20GB+ disk)
- [ ] Install a temporary Linux system (Ubuntu/Debian recommended as host)
- [ ] Download Linux kernel 4.x sources
- [ ] Create partition layout and mount points

### Phase 2: Kernel Compilation

- [ ] Extract kernel sources to `/usr/src/kernel-$(version)`
- [ ] Configure kernel with `make menuconfig`
- [ ] Customize kernel version string with your login
- [ ] Compile kernel: `make` and `make modules`
- [ ] Install kernel and modules

### Phase 3: System Bootstrap

- [ ] Create basic directory structure (FHS compliant)
- [ ] Install bootloader (GRUB recommended)
- [ ] Configure bootloader for your custom kernel
- [ ] Set up initial ramdisk if needed

### Phase 4: Package Installation

## 📦 Mandatory Packages

### Build Tools & Dependencies

- [ ] **Acl** - Access Control Lists
- [ ] **Attr** - Extended attributes utilities  
- [ ] **Autoconf** - Automatic configure script builder
- [ ] **Automake** - Tool for generating Makefile.in files
- [ ] **Binutils** - Collection of binary tools
- [ ] **Bison** - Parser generator
- [ ] **GCC** - GNU Compiler Collection
- [ ] **Make** - Build automation tool
- [ ] **M4** - Macro processor

### Core System

- [ ] **Bash** - Bourne Again SHell
- [ ] **Bc** - Basic calculator
- [ ] **Bzip2** - Data compression program
- [ ] **Check** - Unit testing framework for C
- [ ] **Coreutils** - Basic file, shell and text manipulation
- [ ] **DejaGNU** - Testing framework
- [ ] **Diffutils** - File comparison utilities
- [ ] **Findutils** - File search utilities
- [ ] **Flex** - Fast lexical analyzer generator
- [ ] **Gawk** - GNU implementation of AWK
- [ ] **Grep** - Text search tool
- [ ] **Gzip** - Data compression program
- [ ] **Sed** - Stream editor
- [ ] **Tar** - Archive utility

### Libraries & Development  

- [ ] **Eudev** - Device manager (alternative to udev)
- [ ] **E2fsprogs** - Ext2/3/4 filesystem utilities
- [ ] **Expat** - XML parser library
- [ ] **Expect** - Program to automate interactions
- [ ] **File** - File type identification utility
- [ ] **GDBM** - GNU database manager
- [ ] **Gettext** - Internationalization utilities
- [ ] **Glibc** - GNU C Library
- [ ] **GMP** - GNU Multiple Precision Arithmetic Library
- [ ] **Gperf** - Perfect hash function generator
- [ ] **Groff** - Document formatting system
- [ ] **GRUB** - Grand Unified Bootloader
- [ ] **Iana-Etc** - Data for /etc/protocols and /etc/services
- [ ] **Inetutils** - Network utilities
- [ ] **Intltool** - Internationalization tool collection
- [ ] **IPRoute2** - Advanced IP routing utilities
- [ ] **Kbd** - Keyboard utilities
- [ ] **Kmod** - Kernel module handling utilities
- [ ] **Less** - Text pager
- [ ] **Libcap** - POSIX capabilities library
- [ ] **Libpipeline** - Pipeline manipulation library
- [ ] **Libtool** - Generic library support script
- [ ] **Man-DB** - Manual page database
- [ ] **Man-pages** - Linux manual pages
- [ ] **MPC** - Multiple precision complex arithmetic library
- [ ] **MPFR** - Multiple precision floating-point library
- [ ] **Ncurses** - Terminal control library
- [ ] **Patch** - Apply patches to files
- [ ] **Perl** - Practical Extraction and Report Language
- [ ] **Pkg-config** - Library compilation flags helper
- [ ] **Procps** - Process monitoring utilities
- [ ] **Psmisc** - Process management utilities
- [ ] **Readline** - Command line editing library
- [ ] **Shadow** - Password and account management
- [ ] **Sysklogd** - System logging daemon
- [ ] **Sysvinit** - System V init
- [ ] **Tcl** - Tool Command Language
- [ ] **Texinfo** - Documentation system
- [ ] **Time Zone Data** - Timezone information
- [ ] **Udev-lfs Tarball** - Device manager for LFS
- [ ] **Util-linux** - System utilities
- [ ] **Vim** - Vi IMproved text editor
- [ ] **XML::Parser** - Perl XML parser
- [ ] **Xz Utils** - Data compression utilities
- [ ] **Zlib** - Compression library

## 🔧 Build Process Tips

### General Build Steps

- [ ] Download source code for each package
- [ ] Extract to appropriate directory
- [ ] Configure with `./configure --prefix=/usr`
- [ ] Compile with `make`
- [ ] Install with `make install`
- [ ] Clean up source directory

### Important Notes

- [ ] Build packages in dependency order
- [ ] Some packages require special configure flags
- [ ] Test critical packages before proceeding
- [ ] Keep build logs for troubleshooting
- [ ] Create backup points during build process

## 🎉 Bonus Features

Once you have a stable system, enhance it with:

- [ ] **X Server** - Graphical display server
- [ ] **Window Managers**: i3, dwm, or others  
- [ ] **Desktop Environments**: GNOME, LXDE, KDE
- [ ] **Additional Software**: Whatever you want!
- [ ] **Custom Configurations**: Make it truly yours

## 📝 Final Checklist

### System Validation

- [ ] System boots successfully
- [ ] Network connectivity works
- [ ] All required packages installed
- [ ] Hostname set correctly
- [ ] Kernel version includes student login
- [ ] Bootloader configured properly
- [ ] File system hierarchy is FHS compliant

### Testing

- [ ] Basic commands work (ls, cat, grep, etc.)
- [ ] Package manager functions (if implemented)
- [ ] Network tools functional
- [ ] System logs properly
- [ ] User management works

## 🚨 Common Issues & Solutions

### Build Problems

- **Dependency errors**: Check build order
- **Missing headers**: Install development packages
- **Compilation fails**: Check configure flags
- **Out of space**: Monitor disk usage

### Boot Problems

- **Kernel panic**: Check kernel config
- **Missing modules**: Verify module installation
- **Boot loader issues**: Check grub configuration
- **File system errors**: Verify partition setup
