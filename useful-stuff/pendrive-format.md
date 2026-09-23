# Formatting a pendrive

1. Find the drive:
```bash
lsblk
```
Match the device by its size (like `sdb1`). Make sure not to select your OS drive.

2. Unmount it if it's currently mounted:
```bash
sudo umount /dev/sdX1
```

3. Format to your preferred filesystem:

FAT32 (broad compatibility):
```bash
sudo mkfs.vfat -F 32 -n "MY_DRIVE" /dev/sdX1
```

exFAT (good for large files, cross-platform):
```bash
sudo mkfs.exfat -n "MY_DRIVE" /dev/sdX1
```

ext4 (Linux only):
```bash
sudo mkfs.ext4 -L "MY_DRIVE" /dev/sdX1
```

4. Flush disk cache before removing:
```bash
sync
```
