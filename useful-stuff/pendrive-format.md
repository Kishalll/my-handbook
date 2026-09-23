# Formatting a pendrive

1. Find the drive:
```bash
lsblk
```
Identify the drive letter (such as `sda` or `sdb`) by its size. Double check so you never touch your main OS drive.

2. Unmount any active partitions:
```bash
sudo umount /dev/sdX*
```

3. Wipe old signatures and ISO headers:
```bash
sudo wipefs --all --force /dev/sdX
```

4. Create a fresh MBR partition table and partition:
```bash
sudo parted /dev/sdX --script mklabel msdos mkpart primary fat32 1MiB 100%
```

5. Format the partition to your preferred filesystem:

FAT32 (broad compatibility, supports UEFI boot):
```bash
sudo mkfs.vfat -F 32 -n "DRIVE_NAME" /dev/sdX1
```

exFAT (for files larger than 4GB, cross-platform):
```bash
sudo mkfs.exfat -n "DRIVE_NAME" /dev/sdX1
```

ext4 (Linux only):
```bash
sudo mkfs.ext4 -L "DRIVE_NAME" /dev/sdX1
```

6. Flush cache before unplugging:
```bash
sync
```

---

### Flashing an ISO directly (alternative)

To write a bootable OS image to the drive using dd:
```bash
sudo dd if=path/to/image.iso of=/dev/sdX bs=4M status=progress oflag=sync
```
Note: Target the entire drive (`/dev/sdX`), not a partition (`/dev/sdX1`).
