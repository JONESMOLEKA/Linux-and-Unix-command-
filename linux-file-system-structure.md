![linuxDir](https://user-images.githubusercontent.com/29688323/106141673-745a5d80-6196-11eb-9643-6845f7cfbf21.jpg)

**1. / (Root)**: Primary hierarchy root and root directory of the entire file system hierarchy.

- Every single file and directory starts from the root directory
- Only root user has the right to write under this directory
- /root is root user’s home directory, which is not same as /

**2. /bin** : Essential command binaries that need to be available in single user mode; for all users, e.g., cat, ls, cp.

- Contains binary executables
- Common linux commands you need to use in single-user modes are located under this directory.
- Commands used by all the users of the system are located here e.g. ps, ls, ping, grep, cp

**3. /boot** : Boot loader files, e.g., kernels, initrd.

- Kernel initrd, vmlinux, grub files are located under /boot
- Example: initrd.img-2.6.32-24-generic, vmlinuz-2.6.32-24-generic