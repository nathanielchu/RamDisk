# OSPRD

OSPRD is a Linux kernel module that implements a ramdisk: an in-memory block device.

## Overview

OSPRD supports read and write operations, as well as a read/write locking feature, where a process can gain exclusive access to the ramdisk.
Like most device drivers, OSPRD can support several of these devices simultaneously; in particular, it supports four simultaneous ramdisks.

OSPRD is a block device, meaning it will implement the Linux block device interface. This allows the ramdisk to be used anywhere a physical block device can be used. 

As a kernel module, OSPRD can be loaded/unloaded into kernel dynamically to change the kernel behavior without needing to reboot the system.

## Features

- Supports read and write operations
- Configurable option to switch between synchronization using blocking and nonblocking locks
- Implements check for 2-process deadlock

## Installation

Extract into ubuntu distribution and run in QEMU emulator with `./run-qemu`.
