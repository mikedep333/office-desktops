# office-desktops
Ansible repo for managing a few shared office desktops

# Prerequisites

1. Since they are all chrometops that are out of support, replace firmware with [standard UEFI compliant firmware from MrChromebox.](https://mrchromebox.tech/). It fixes the graphics output problem on Acer Chrometop 24 All-In-Ones ("Buddy")
1.  Install Fedora 34 Workstation, MATE,etc. Since they have 16GB storage, EFI partition to 200MB, boot partition to 400MB, and Btrfs (for compression later.) Set /usr, /opt and /home to subvolumes for (likely) easier compression policies (1 desktop has /usr and /opt not on subvolumes though.) User `coreos`, with admin rights.
1.  `sudo hostnamectl set-hostname <office-room-name>`
1.  `sudo systemctl enable --now sshd.socket`
1.  Use the GNOME control center (Users) or the MATE login config app to set automatic login.
1.  Use the GNOME control center (Privacy -> Screen Lock) or the MATE Screensaver config app to not lock while idle.
1.  Add the user to `systemd-journal` group.
