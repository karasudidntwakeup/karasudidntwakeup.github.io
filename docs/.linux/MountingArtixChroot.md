+ `sudo cryptsetup open /dev/nvme0n1p2 karasu`

+ `sudo mount /dev/mapper/karasu /mnt`

+ `sudo mount /dev/nvme0n1p1/mnt/boot`

+ `sudo mount --bind /dev /mnt/dev`

+ `sudo mount --bind /proc /mnt/proc`

+ `sudo mount --bind /sys /mnt/sys`

+ `sudo mount -t devpts devpts /mnt/dev/pts`

+ `sudo mount -t  efivarfs /sys/firmware/efi/efivars /mnt/sys/firmware/efi/efivars`

+ `sudo chroot /mnt`

+ `grub-install --target=x86_64-efi --efi-directory=/boot`

+ `grub-mkconfig -o /boot/grub/grub.cfg`

 + exit

+ `umount -R /mnt`
