Login and start ```setup```

Select Language

Select ```Prepare Instalation```

Select ```Set Virtual Console``` and change to yours

Check if your partition is showing in ```List Devices```

Select ```Partition Disk``` and select the disk

Select ```Automatic Partitioning``` and choose yes.

Go ```Back``` and Select ```Mount Paritions```

Mount the root partition, select ```ext4``` confirm

Select ```noatime```. If you have SSD select ```discard``` aswell. Confirm.

Choose your SWAP partition, pick the same size of your RAM or ```8G``` if you have more than 8GB of RAM

Select ```done``` and choose your UEFI partition and select ```/boot/efi```

Select ```Configure Installer Mirrorlist``` and ```Edit Pacman Configuration```

Uncomment or add ```Color``` and ```ILoveCandy``` under the ```# Misc options```

Uncomment the ```[multilib]``` repo and add the repos in the repos.txt in this repo, save and quit

Select ```Yes``` to use the edited pacman configuration

Select ```Edit Pacman Mirror Configuration```

Uncomment or add ```Branch = stable```, ```Method = rank```, ```Protocols = ftp,https,http``` and ```SSLVerify = True```, save and quit

Select ```Rank Mirrors by Speed``` select ```stable``` when it's done, select the first 50 mirrors

Select ```Back``` then ```Refresh Pacman Keys```

Select ```Choose pacman cache``` and select ```Yes```

Select ```Enable fsck hook``` and select ```Yes```

Select ```Back```, select ```Install Desktop System```, select ```Install Manjaro Desktop```

Select ```yay + base-devel```, ```linux-lts```, a stable kernel (```linux54``` is the latest stable as of writting this) and the latest one without the ```-rt``` suffix

Choose your desktop environment and select ```Yes``` to choose additional packages

Packages:

```fish```

```gedit```

```git```

```code```

```xclip```

```rustup```

```noto-fonts```

```noto-fonts-cjk```

```noto-fonts-emoji```

```noto-fonts-extra```

```firefox-developer-edition```

```ttf-fira-code```

```yakuake```

```phonon-qt5-vlc```

Select the ```minimal``` version

Select ```Auto-install proprietary drivers```

Select ```Install Bootloader```, select ```grub``` and select ```yes``` to set as default bootloader

Select ```Configure Base``` and select ```Generate FSTAB```

Select ```fstabgen -U -p```

Select ```Set Hostname``` and choose a name

Select ```Set System Locale``` select ```en_US.UTF-8``` for locale and choose your own for Time and Date

Select ```Set Desktop Keyboard Layout``` and select yours

Select ```Set Timezone and Clock``` and choose accordingly, if you're dualbooting with Windows, choose ```localtime```

Select ```Set Root Password``` and set it

Select ```Add new user``` and add it

Select ```fish``` as default shell and set your user's password

Select ```Back```, ```System Tweaks``` and ```Security and systemd Tweaks```

Select ```Amend journald Logging``` and choose ```200M```

Select ```Disable Coredump Logging``` and choose ```Disable```

Select ```Restrict Access to Kernel Logs``` and choose ```Disable```

Go ```Back```, ```Back``` and ```Back``` and select  ```Done```

Select ```Yes``` to close the installer

Select ```No``` to save log

Remove USB stick, CD, etc and reboot



In the OS open terminal and type ```rm .b* .z

If you don't have a ```sddm.conf``` in you ```/etc/``` folder type the following in your terminal:

Type ```sddm --example-config | sudo tee /etc/sddm.conf```

Then edit it and set ```MinimumVT``` to 7, save and quit

Type ```yay --nodiffmenu --editmenu --save``` and done.



Proceed to install your Post Install Scripts
