# Solution – Walking Dead

## Step 1: Inspect Partition Table
Run:
fdisk -l walking_dead_250.img

Observation:
Only FAT32 partition is visible.

---

## Step 2: Identify Hidden Partitions
Use:
mmls walking_dead_250.img

This reveals additional unallocated regions where deleted partitions exist.

---

## Step 3: Recover ext4 Partition
Mount using offset:
mount -o loop,offset=<offset> walking_dead_250.img /mnt/ext4

Retrieve:
part1.txt → GDG{Und3ad_

---

## Step 4: Recover NTFS Partition
Mount or carve using:
photorec

Retrieve:
part2.txt → Part1t10n_Fr4gm3nt}

---

## Step 5: Reconstruct Flag
Combine both parts:

GDG{Und3ad_Part1t10n_Fr4gm3nt}

---

## Key Learning
Understanding partition structures and analyzing unallocated space is critical in forensic investigations.
