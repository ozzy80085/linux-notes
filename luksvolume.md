# LUKS volume in ubuntu
*to decrypt the volume:*

    sudo cryptsetup open /dev/sdX secret
	
   
you will be prompted for a password

*to mount the volume:*

    sudo  mount /dev/mapper/secret  /mnt/

---
*to encrypt the volume:*

    cryptsetup close secret

to unmount the volume:

    sudo umount /dev/sdX
