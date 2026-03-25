# 🧟 Walking Dead – Disk Forensics Challenge

## Category
Forensics / Disk Analysis

## Difficulty
Medium

## Description
A raw disk image where only a FAT32 partition appears in the partition table. However, additional ext4 and NTFS partitions were intentionally removed and contain hidden fragments of the flag.

Participants must analyze unallocated space, recover deleted partitions, and reconstruct the full flag.

## Skills Tested
- Partition table analysis (MBR)
- Identifying hidden/unallocated space
- Mounting partitions using offsets
- File recovery and carving
- Evidence reconstruction

## Tools Suggested
fdisk, mmls, Autopsy, photorec
