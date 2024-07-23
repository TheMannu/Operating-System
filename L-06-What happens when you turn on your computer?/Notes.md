# PC Boot Process

## i. PC On
- The user turns on the PC.

## ii. CPU Initialization
- The CPU initializes itself and looks for a firmware program (BIOS) stored in the BIOS Chip.
  - The BIOS Chip (Basic Input-Output System Chip) is a ROM chip found on the motherboard that allows access and setup of the computer system at the most basic level.
  - In modern PCs, the CPU loads UEFI (Unified Extensible Firmware Interface).

## iii. BIOS/UEFI Execution
- The CPU runs the BIOS, which tests and initializes system hardware.
- BIOS loads configuration settings.
  - If something is not appropriate (e.g., missing RAM), an error is thrown, and the boot process stops.
  - This is called the POST (Power-On Self-Test) process.

> UEFI can do a lot more than just initialize hardware; it’s really a tiny operating system. For example, Intel CPUs have the Intel Management Engine. This provides a variety of features, including powering Intel’s Active Management Technology, which allows for remote management of business PCs.

## iv. Handoff to Bootloader
- BIOS hands off responsibility for booting your PC to your OS’s bootloader.
  - BIOS looks at the MBR (Master Boot Record), a special boot sector at the beginning of a disk.
    - The MBR contains code that loads the rest of the operating system, known as a “bootloader.”
    - BIOS executes the bootloader, which takes it from there and begins booting the actual operating system—Windows or Linux, for example.

> In other words, the BIOS or UEFI examines a storage device on your system to look for a small program, either in the MBR or on an EFI system partition, and runs it.

## v. Bootloader Execution
- The bootloader is a small program that has the large task of booting the rest of the operating system.
  - It boots the kernel and then the user space.
  - Different operating systems use different bootloaders:
    - **Windows**: Windows Boot Manager (`Bootmgr.exe`)
    - **Linux**: GRUB (GRand Unified Bootloader)
    - **Macs**: `boot.efi`
