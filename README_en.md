# Preface

This document is intended for first-time Arch installers.

What is Arch?

Arch is a DIY (Do It Yourself) Linux operating system where users install everything themselves. Those who use it are often referred to as "enthusiasts" because they enjoy the thrill of customizing everything.

Apart from the enthusiast appeal, Arch stands out from other Linux operating systems in the following ways:

1. All packages are the latest versions.
2. A single command updates all packages to the latest version.
3. The environment is minimal and clean because users install everything from scratch.
These distinctive features, along with its user-friendly nature, make Arch a popular choice among many users.



# Catalog
- [Download ISO files](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E4%B8%8B%E8%BC%89iso%E5%AE%89%E8%A3%9D%E6%AA%94)
- [Arch Reference](https://github.com/sheucm/Arch-Installation/blob/master/README.md#arch%E5%8F%83%E8%80%83%E6%96%87%E4%BB%B6)
- [Install Arch Linux](https://github.com/sheucm/Arch-Installation/blob/master/README.md#arch%E5%8F%83%E8%80%83%E6%96%87%E4%BB%B6)
- [Add User](https://github.com/sheucm/Arch-Installation/blob/master/README.md#add-user)
- [Delete User](https://github.com/sheucm/Arch-Installation/blob/master/README.md#delete-user)
- [Install package](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%AE%89%E8%A3%9Dpackage)
- [Install Desktop GUI](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%AE%89%E8%A3%9Ddesktop-gui)
- [Enable/Disable Service](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%95%9F%E5%8B%95%E6%88%96%E9%97%9C%E9%96%89service)
- [System Upgrade](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E7%B3%BB%E7%B5%B1%E7%B8%BD%E6%9B%B4%E6%96%B0)
- [~/.bashrc](https://github.com/sheucm/Arch-Installation/blob/master/README.md#bashrc)
- [VirtualBox Shared Folder Settings](https://github.com/sheucm/Arch-Installation/blob/master/README.md#virtualbox%E5%85%B1%E7%94%A8%E8%B3%87%E6%96%99%E5%A4%BE%E8%A8%AD%E5%AE%9A)
- [VirtualBox Two-way clipping](https://github.com/sheucm/Arch-Installation/blob/master/README.md#virtualbox%E9%9B%99%E5%90%91%E5%89%AA%E8%B2%BC)
- [VirtualBox Plug in Usb](https://github.com/sheucm/Arch-Installation/blob/master/README.md#virtualbox%E6%8F%92%E5%85%A5usb)
- [Install Chrome](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%AE%89%E8%A3%9Dchrome%E7%80%8F%E8%A6%BD%E5%99%A8)
- [Other Common Installation](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%85%B6%E5%AE%83%E5%B8%B8%E7%94%A8%E5%AE%89%E8%A3%9D)
- [Install Chinese Font](https://github.com/sheucm/Arch-Installation/blob/master/README.md#install-chinese-fonts)
- [Set up Chinese graphical interface](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E8%A8%AD%E5%AE%9A%E5%9C%96%E5%BD%A2%E5%8C%96%E4%B8%AD%E6%96%87%E4%BB%8B%E9%9D%A2)
- [Install Chinese input method](https://github.com/sheucm/Arch-Installation/blob/master/README.md#install-chinese-keyboard)
- [Set Time](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E8%A8%AD%E5%AE%9A%E6%99%82%E9%96%93)
- [Set audio output and microphone input](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E8%A8%AD%E5%AE%9A%E9%9F%B3%E8%A8%8A%E8%BC%B8%E5%87%BA%E8%88%87%E9%BA%A5%E5%85%8B%E9%A2%A8%E8%BC%B8%E5%85%A5)
- [Install USB interface](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%AE%89%E8%A3%9Dusb%E4%BB%8B%E9%9D%A2)
- [System backup and restore](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%82%99%E4%BB%BD%E8%88%87%E9%82%84%E5%8E%9F)
- [Install Nvidia 3D acceleration driver](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%AE%89%E8%A3%9Dnvidia-3d-%E5%8A%A0%E9%80%9F-driver)
- [Install Firewall](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%AE%89%E8%A3%9D%E9%98%B2%E7%81%AB%E7%89%86)
- [Adjust the appearance of Xfce terminal](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E8%AA%BF%E6%95%B4xfce-terminal%E5%A4%96%E8%A7%80)
- [Set terminal shortcut keys](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E8%A8%AD%E5%AE%9Aterminal%E5%BF%AB%E6%8D%B7%E9%8D%B5)
- [Change desktop background](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E6%8F%9B%E8%83%8C%E6%99%AF)
- [Advanced Xfce appearance settings](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E9%80%B2%E9%9A%8Exfce%E5%A4%96%E8%A7%80%E8%A8%AD%E5%AE%9A)
- [Can I use something like Microsoft Office on Arch?](https://github.com/sheucm/Arch-Installation/blob/master/README.md#arch%E4%B8%8A%E5%8F%AF%E4%BB%A5%E7%94%A8%E9%A1%9E%E4%BC%BC%E5%BE%AE%E8%BB%9Foffice%E5%97%8E)
- [Watch hard drive usage](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E8%A7%80%E7%9C%8B%E7%A1%AC%E7%A2%9F%E4%BD%BF%E7%94%A8%E7%8E%87)
- [Add Network DNS](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%A2%9E%E5%8A%A0network-dns)

# Download ISO files
- Please go to [this official website](https://www.archlinux.org/download/) to download the torrent file and use torrent software to download the iso file.
- Burn the iso file to a disc or usb, and make the disc drive or usb the first priority when booting

# Arch Reference
- [Frequently asked questions](https://wiki.archlinux.org/index.php/Frequently_asked_questions)
- [Installation guide](https://wiki.archlinux.org/index.php/Installation_guide)
- [Users and groups](https://wiki.archlinux.org/index.php/users_and_groups)
- [General recommendations](https://wiki.archlinux.org/index.php/General_recommendations)
- [pacman](https://wiki.archlinux.org/index.php/pacman)

# Install Arch Linux

For detailed installation instructions, you can watch [**this video**](https://www.youtube.com/watch?v=4PBqpX0_UOc):100:


The installation process is recorded in text below:
- After booting, you will find a menu. Please select the **Boot Arch Linux** menu.
- Then you will enter command line mode as root

### Part 0: Preset settings
- To view the current disk status, please issue the command `lsblk`. You will see the status of your hard drive, usually you will see the words sda or sdb. Assume that the disk to be installed in this article is called sda.
- Check whether the hard drive is UEFI (you don’t need to know what this is). If it is UEFI, this article does not apply.
     How to check? Type the command `ls /sys/fireware/efi/efivars`. If No such file or directory comes out, then you are right. On the other hand, if a lot of files are generated, then your disc is UEFI and this tutorial does not apply.
- Check if there is internet. Type the command `ping www.google.com`.
- Set time: enter the command `timedatectl set-ntp true`

### Part 1: Split hard drive
- Enter the command `fdisk /dev/sda` to prepare for splitting (if yours is sdb, change it to sdb).
- You can enter m at this time to view the instructions. (Simple operation instructions: `p` prints out the disk status; `d` deletes the existing disk partition; `n` adds a new partition; `w` writes the changes to the disk)
- Press `n` first to add a partition for boot:
     - Partition Type: p
     - Partition Number: (default, press enter)
     - First sector: (default, press enter)
     - Last sector: +200M (at least 200)
- At this point `p`, you can see the new split displayed on the screen.
- Press `n` again to add a new partition for swap:
     - Partition Type: p
     - Partition Number: (default, press enter)
     - First sector: (default, press enter)
     - Last sector: +2G (most people recommend ram size * 150%, assuming 8G ram, swap is set to 12G)
- Press `n` again to create a new partition for root:
     - Partition Type: p
     - Partition Number: (default, press enter)
     - First sector: (default, press enter)
     - Last sector: +25G (recommend at least 25G)
- Press `n` again to add a new partition for home:
     - Partition Type: p
     - Partition Number: (default, press enter)
     - First sector: (default, press enter)
     - Last sector: (default, press enter)
- At this point, press `p` to see the perfectly divided partitions.
- Press `w` to save all changes. Note: This will permanently erase the disk data.
- Enter the command `lsblk`, and you can see sda1, sda2, sda3, and sda4. And you can see that their capacities are 200M, 2G, 25G, and remaining capacity respectively.
- Next, install file system on sda1, sda3, and sda4:
     - Enter the command `mkfs.ext4 /dev/sda1`
     - Enter the command `mkfs.ext4 /dev/sda3`
     - Enter the command `mkfs.ext4 /dev/sda4`
- Next, mark sda2 as swap:
     - Enter the command `mkswap /dev/sda2`
     - Enter the command `swapon /dev/sda2`
- At this time, type the command `lsblk` and you can see that the MOUNTPOINT column of sda2 has a [SWAP] mark.
- Next, mount sda1, sda3, and sda4.
- First perform the mount action on sda3 (root) and enter the command `mount /dev/sda3 /mnt`.
- Type the command `ls /mnt` to find the lost+found file.
- At this time, type the command `lsblk`, and you can find that the MOUNTPOINT column of sda3 has /mnt.
- Create home and boot folders:
     - Type the command `mkdir /mnt/home`
     - Type the command `mkdir /mnt/boot`
- Perform mount actions for sda1(boot) and sda4(home):
     - Type the command `mount /dev/sda1 /mnt/boot`
     - Type the command `mount /dev/sda4 /mnt/home`
- At this time, type the command `lsblk`, and you can see that the MOUNTPOINT columns of sda1 and sda4 are /mnt/boot and /mnt/home respectively.


### Part 2: install the system
- Install Arch Linux:
     - Enter the command `pacstrap /mnt base base-devel vim` and install vim by the way. (It will take a while)
- Generate fstab, its purpose is to automatically select the correct location to start the Arch operating system when booting.
     - We will use the genfstab command. You can type the command `genfstab` directly and there will be instructions on how to use it.
     - Enter the command `genfstab /mnt`, and you can see the data corresponding to the four sda partitions, but we need to use uuid, which is safer, so...
     - Enter the command `genfstab -U /mnt` and add -U, you can see that the output is changed to uuid.
     - Output it to the /mnt/etc/fstab file and type the command `genfstab -U /mnt >> /mnt/etc/fstab`.
     - Enter the command `vim /mnt/etc/fstab`, the content should contain sda1~4, four pieces of information.
- Next, you need to actually enter the Arch system: enter the command `arch-chroot /mnt`
- At this time, enter the ARCH system from the ISO system to the real DISK installed. So you can type the command `vim /etc/fstab` to view the fstab file just created.

### part 3: Install network
- Type the command `pacman -S networkmanager`
- Start network manager. Type the command `systemctl enable NetworkManager`
- Install grub, which is a bootloader.
     - Type the command `pacman -S grub`
     - Enter the command `grub-install --target=i386-pc /dev/sda` (note: not sda1, not sda2...)
     - If there is no error, generate the grub config file again and enter the command `grub-mkconfig -o /boot/grub/grub.cfg`

### Part 3: Settings
-Set the root password, enter the command `passwd`, and enter your own password.
- Enter the command `nano /etc/locale.gen`, use nano or vim editor to edit the locale.gen file, find the following language, remove the #, save and exit:
     - zh_TW.big5
     - zh_TW.utf8
     - en_US.iso88591
     - en_US.utf8
- Enter the command `locale-gen` to generate locale.
- Move to the `/usr/share/zoneinfo/` directory and you can see many time zones. In terms of Taiwan, it belongs to `Asia/Taipei`. So please type the command `ln -sf /usr/share/zoneinfo/Asia/Taipei /etc/localtime`.

- Type the command `vim /etc/hostname`, enter the file, type your own hostname (get it yourself), save and leave.
- Type the command `exit` to leave the disk Linux system
- Leave mount and type the command `umount -R /mnt`
- Enter the command `lsblk`, and you can see the MOUNTPOINT of sda1~4. Only sda2 writes SWAP, and the others are blank.
- Enter the command `shutdown now` to shut down.
- Uninstall the installation file (iso) and reboot.
- Enter grub selection and select the default *Arch Linux*. Even if you don't choose, you will enter by yourself in a few seconds.
- Login as root, and the password as you just set.
- The installation is complete.

# Add User
For detailed information, please refer to [Arch Wiki - Users and Groups](https://wiki.archlinux.org/index.php/users_and_groups) :thumbsup:

The following simply creates a new User named eric as an example, and can use sudo permissions:
- Log in with root account.
- You can first enter the command `passwd -Sa` to check the current users. You should see root.
- Enter the command `useradd --create-home -G wheel eric` to create a user named eric with his own home directory. Wheel means he has sudo permissions.
- Type the command `passwd eric` to set the password for this user.
- Enter the command `visudo` and find the line of code *root ALL=(ALL) ALL*. Add `eric ALL=(ALL) ALL` below it (or remove the # from `#%wheel ALL=(ALL) ALL` below, that's fine), then save and leave. If you don’t know how to use the vi editor, please google it yourself.
- Type the command `exit`, leave root, and log in with the eric account.
- Type the command `pwd` to see if it is in the `/home/eric` directory.
- Enter the command `sudo -s` to test whether you have root permissions successfully.
- Finish.

# Delete User
If you want to delete a user, you can use the `userdel` command. Take the eric user in the previous section as an example. If you want to delete eric:
- Log in as root.
- Enter the command `userdel -r eric` to delete user eric. `-r` means to delete including home directory and mail.
- Enter the command `passwd -Sa`, you should not see eric anymore.
- Enter the command `ls /home`, you should not be able to see eric's folder.
- Finish.


# Install package

### Official download

You can go to [this arch website](https://www.archlinux.org/packages/) to find out whether the package you want is officially provided. If so, you can:

- Installation: Type the command `pacman -S <package_name>`
- Search: Type the command `pacman -Sl | grep <package_name>`
- Uninstall: type the command `pacman -Rs <package_name>`

If you have used ubuntu or other linus systems before, you can read [this table](https://wiki.archlinux.org/index.php/Pacman/Rosetta) to learn the pacman command faster.

### Manual installation

- Find the installation repo of <package>
- clone to local. Type the command `git clone <package-repo>`
- Enter the project. Type the command `cd <package>`
- Create installation files. Type the command `makepkg -s`. Finally, you will see an installation file similar to <package>.pkg.tar.xz in the directory.
- Install. Type the command `sudo pacman -U <package>.pkg.tar.xz`
- The installation is complete.
- Uninstall: type the command `pacman -Rsn <package_name>`

### More about pacman
- `$ man pacman`
- `$ pacman --help`
- [Pacman - ArchWiki](https://wiki.archlinux.org/index.php/pacman)

# Install Desktop GUI
- You can refer to this video: [After a Minimal Linux Install: Graphical Envionment and Users](https://www.youtube.com/watch?v=nSHOb8YU9Gw) :thumbsup\_tone3:
- Install x.org. Type the command `pacman -S xorg-server xorg-xinit`. Whether you want to install Desktop or Window, you must install xorg.
- Install xfce Desktop. Type the command `pacman -S xfce4`
- Set up **.xinitrc** file. Add the line `exec xfce4-session` to the `~/.xinitrc` file.
- Type the command `startx` to enter the GUI interface.
- Install display manager (referred to as dm):
     - Enter the command `sudo pacman -S lightdm lightdm-gtk-greeter`
     - Enter the command `sudo systemctl enable ligthdm.service` to tell the system to start lightdm every time it is powered on.

     Supplement: DM means that when you log in, there will be a GUI interface to select the logged in user, and you can enter the login password in the DM interface. If you don't want to install dm, you can just enter the tty mode and log in every time you boot, and then type the startx command to enter the GUI interface.

# Enable/Disable Service
- Start: Enter the command `sudo systemctl start <service>`
- Shut down: Enter the command `sudo systemctl stop <service>`

# System Upgrade
Update all packages using official downloads.
Type the command `$ sudo pacman -Syyu`.

# ~/.bashrc
`~/.bashrc` can ask the system to execute the script in this file after booting.
For example, I want to set alias, environment variables, etc. here.

# VirtualBox Shared Folder Settings
- First add a folder to be shared on this machine. For example: `D:\VirtualBoxShareArch`
- Start arch, click **Device** -> **Shared Folder** -> **Shared Folder Settings** in the window index bar, click + Add Folder on the right, and select D:\VirtualBoxShareArch folder, check the "Automount" and "Make permanent" options and press OK.
- Install virtualbox guest addition:
     - Enter the command `sudo pacman -Sl | grep virtualbox`, and you can see that there are related packages that can be installed.
     - Enter the command `sudo pacman -S virtualbox-guest-modules-arch`
     - Enter the command `sudo pacman -S virtualbox-guest-utils`
- restart.
- Add a new shared folder for arch. For example: `/home/eric/Desktop/share`
- Enter the command `sudo mount -t vboxsf VirtualBoxShareArch /home/eric/Desktop/share`. At this time, the share folder on Arch is shared with the VirtualBoxShareArch folder on this machine.
- Finish

# VirtualBox Two-way clipping
- **VirtualBox Shared Folder Settings** steps must be completed
- Off state
- Click on the machine's "Settings" -> General -> Advanced:
     - Shared clipboard: two-way
     - Drag and drop: both directions
- Finish

# VirtualBox Plug in Usb
- Download [VirtualBox Extension Pack](https://www.virtualbox.org/wiki/Downloads) and install
- Restart virtualbox
- Press "Settings" -> "USB" for its virtual machine and select "*USB 3.0 (xHCI) Controller*". (If it is usb2.0, choose 2.0)
- Power on
- In the menu at the top of the window, click "Device" -> "USB" and select the USB device you inserted. In this way, it is like a USB plugged into this virtual machine.
- Check: Open the terminal and type the command `$lsblk`. If you see something like sdb, sdc, etc., check to see if the capacity is the size of your own USB. If so, you are right.

# Install Chrome
- [Reference article](https://linuxhint.com/install-google-chrome-on-arch-linux/)
- Requirements: To install git
- installation steps:
     - `$ git clone https://aur.archlinux.org/google-chrome.git`
     - `$ cd google-chrome/`
     - `$ makepkg -s`
     - `$ sudo pacman -U google-chrome-63.0.3239.108-1-x86_64.pkg.tar.xz`
     - After the installation is complete, click Application -> Internet -> Google Chrome in the upper left corner to start the browser.

# Other Common Installation
- git
- gedit (text editor)
- wget (download command tool)
- unzip (zip decompression command tool)
- firefox (Firefox browser)
- [deepin-screenshot](https://www.archlinux.org/packages/?name=deepin-screenshot) (Screenshot GUI tool)
- [gpicview](https://www.archlinux.org/packages/community/x86_64/gpicview/) (picture viewer)
- [net-tools](https://www.archlinux.org/packages/core/x86_64/net-tools/)(ifconfig command)
- [nmap](https://www.archlinux.org/packages/extra/x86_64/nmap/)(nmap command)
- [bind-tools](https://www.archlinux.org/packages/extra/x86_64/bind-tools/)(dig command)

```bash
$ sudo pacman -S <package>
```

#Install Chinese Fonts
- [Arch Fonts](https://wiki.archlinux.org/index.php/fonts)
- **Download all following Chinese Fonts !** :
     - adobe-source-han-sans-cn-fonts
     - adobe-source-han-sans-tw-fonts
     - adobe-source-han-serif-cn-fonts
     - adobe-source-han-serif-tw-fonts
     -wqy-microhei
     -wqy-zenhei
     -wqy-bitmapfont
     -ttf-arphic-ukai
     -ttf-arphic-uming
     -opendesktop-fonts
     -ttf-hannom
    
     ```bash
     $ sudo pacman -S <font-package>
     ```
    
- Need to manually install yourself:
     - Manual Chinese font lists with its repo URL:
         - [**ttf-tw**](https://aur.archlinux.org/packages/ttf-tw/): https://aur.archlinux.org/ttf-tw.git
         - [**noto-fonts-sc**](https://aur.archlinux.org/packages/noto-fonts-sc/): https://aur.archlinux.org/noto-fonts-sc.git
         - [**noto-fonts-tc**](https://aur.archlinux.org/packages/noto-fonts-tc/): https://aur.archlinux.org/noto-fonts-tc.git
     - Install Steps:
         - Copy repo URL
         - Clone it to local. `$ git clone <repo-url>`
         - Go into the directory. `$ cd <repo-directory>`
         - Make package. `$ makepkg -s`
         - Install the package. `$ sudo pacman -U <package_name>-any.pkg.tar.xz`
         - Reboot your arch. `$ reboot`
         - Finished Installing that ttf !
- Reboot your arch. `$ reboot`

# Set up Chinese graphical interface
- Preface: If you feel that the Arch system is always displayed in English and want to change it to Chinese, you can refer to the settings in this article.
- Reference article:
     - [Locale - ArchWiki](https://wiki.archlinux.org/index.php/locale)
     - [Localization/Traditional Chinese](https://wiki.archlinux.org/index.php/Localization/Traditional_Chinese_(%E6%AD%A3%E9%AB%94%E4%B8%AD%E6%96%87 ))
- Requirements: Chinese fonts must be installed.
- Steps to set up Chinese interface:
     - Enter the command `$ locale -a` and check whether zh_TW.utf8 appears. If not, please follow the instructions in the *reference article* to generate the Chinese language family.
     - Edit /etc/locale.conf
     - Change it to `LANG=zh_TW.UTF-8`
     - restart

# Install Chinese input method (Optional)
- [Arch Fxitx](https://wiki.archlinux.org/index.php/Fcitx)
- Other Article: [Installing fcitx](http://echoyun.com/2017/10/02/installing-fcitx-chinese-ime-arch-linux/)
- Requirements: Chinese fonts should be installed.
- **Download traditional Chinese Keyboard**:
     - fxitx
     -fcitx-chewing
     - fcitx-table-extra (if you want to use [Boshiamy](https://en.wikipedia.org/wiki/Boshiamy_method))
     -fcitx-im
     -fcitx-configtool
    
     ```bash
     $ sudo pacman -S fcitx fcitx-chewing fcitx-table-extra fcitx-im fcitx-configtool
     ```
- Set *.xinitrc* file:
     - `$ sudo vim /root/.xinitrc`
     - Edit like this:
    
     ```
     # .xinitrc
     export GTK_IM_MODULE=fcitx
     export QT_IM_MODULE=fcitx
     export XMODIFIERS=@im=fcitx
     ```
- Reboot your arch. `$ reboot`
- Open fcitx-configtool. `$ fcitx-configtool`
-Add your favorite input methods
- Done. (I can finally type Chinese!!)

# Set Time
If you find that the time in the upper right corner is wrong, you can follow the following instructions to set the time:

```bash
# timedatectl set-time "yyyy-MM-dd hh:mm:ss"
$ timedatectl set-time "2018-10-204 17:56:54"
```

Reference [Arch Time](https://wiki.archlinux.org/index.php/time)


# Set audio output and microphone input
- reference document
     - [Arch - Sound system](https://wiki.archlinux.org/index.php/sound_system)
     - [Arch - Advanced Linux Sound Architecture](https://wiki.archlinux.org/index.php/Advanced_Linux_Sound_Architecture#Unmuting_the_channels)
     - [Arch - Advanced Linux Sound Architecture/Troubleshooting](https://wiki.archlinux.org/index.php/Advanced_Linux_Sound_Architecture/Troubleshooting#Microphone)
- Note: Alsa Linux Kernal is used to process audio. It is built-in and does not need to be installed. So we need to install its utils, and the default is mute. In the steps, we will explain how to turn off mute.
- Steps:
     - Install alsa utils: `$ sudo pacman -S alsa-utils`. At this time there will be two utilities, namely *alsamixer* and *amixer*.
     - Use alsamixer to unmute: `$ alsamixer`
     - Take a screenshot of the official document description:
    
     ```
     The MM label below a channel indicates that the channel is muted, and 00 indicates that it is open.

     Scroll to the Master and PCM channels with the ← and → keys and unmute them by pressing the m key.

     Use the ↑ key to increase the volume and obtain a value of 0 dB gain. The gain can be found in the upper left next to the Item: field.
     ```
    
     - Press m for Master, then press the up and down keys to adjust the volume.
     - Press m on HeadPhone, then press the up and down keys to adjust the volume.
     - Press m for Front Mic and Front, then press the up and down keys to adjust the volume.
     - Press m on the Rear Mic, then press the up and down keys to adjust the volume.
     - Press f4 to enter the Capture tab, press the Space key for both Captures, and use the up and down keys to adjust the volume.
     -Input Source (there are two) press the up and down keys to change it to Front Mic
     - Press Esc to leave settings
- test:
     - Speaker sound: Go to youtube to test
     - Microphone sound: [Microphone Test](https://www.onlinemictest.com/)
    
# Install USB interface
- Reference [Udisks - ArchWiki](https://wiki.archlinux.org/index.php/Udisks)
- Requirements: Desktop GUI installed
- Steps:
     - Download [udisk2](https://www.archlinux.org/packages/?name=udisks2): `$ sudo pacman -S udisks2`.
     - Type the command `$lsblk` to see which sector number the USB device is in. Assuming the usb device is in /dev/sdb:
     - mount usb: Enter the command `$ udisksctl mount -b /dev/sdb1`
     - unmount usb: Enter the command `$ udisksctl unmount -b /dev/sdb1`
     - Open File Manager and you can see your USB device in the DEVICES area on the far left.
     - Finish.
    
Supplement: I still don’t know how to make it automatically mount the USB device.
    
# System backup and restore
- File reference: [rsync - ArchWiki](https://wiki.archlinux.org/index.php/rsync)
- Video tutorial reference: [Backup and Restore Your Linux System with rsync](https://www.youtube.com/watch?v=oS5uH0mzMTg) :100:
- a:
     - [usb formatted as Ext4](http://www.eassos.com/how-to/how-to-format-a-flash-drive.php).
     - Install [rsync](https://www.archlinux.org/packages/?name=rsync) on arch: `＄ sudo pacman -S rsync`
- Backup steps:
     - turn on arch and plug in usb
     - `$ lsblk`, look at the USB sector (mine is /dev/sdb1)
     - mount usb, `$udisksctl mount -b /dev/sdb1`
     - Backup test:
    
     ```bash
     $ sudo rsync -aAXv --delete --dry-run \
     --exclude=/dev/* --exclude=/proc/* \
     --exclude=/sys/* --exclude=/tmp/* --exclude=/run/* --exclude=/mnt/* \
     --exclude=/media/* --exclude="swapfile" --exclude="lost+found" \
     --exclude=".cache" --exclude="Downloads" --exclude=".VirtualBoxVMs" \
     --exclude=".ecryptfs" \
     /source /destination
     ```
    
     - Explanation of backup test instructions:
         - /source is the root directory to be backed up: replaced by `/`.
         - /destination is the place to backup to: replaced by `/run/media/eric/my_usb`
         - --dry-run. Indicates that it is in the testing stage and has not actually been written to USB. During the testing phase, the console will print out the files to be backed up. You can add `>> log.txt` at the end to see if the files to be backed up are incorrect.
         - For explanations of other parameters, please refer to the video tutorial.
     - Actual backup to USB: Make sure the backup list is OK, remove *--dry-run* and start!
     - Open the USB folder and check if there is a backup in it.
     - unmount usb: `$ udisksctl unmount -b /dev/sdb1`.
    
- Restoration steps:
     - Restart the computer, install the arch iso, and plug in the USB.
     - After booting, the screen will stop at the iso command line, type `$ls`, and you should only see install.txt.
     - Create two folders: `$ mkdir /mnt/system /mnt/usb`
     - `$lsblk`, check whether USB exists and look at the sector number. example:
         - boot: /dev/sda1
         - root: /dev/sda3
         - home: /dev/sda4
         - usb: /dev/sdb1
     -Mount system：
         - `$ mount /dev/sda3 /mnt/system`
         - `$ mount /dev/sda4 /mnt/system/home`
         - `$ mount /dev/sda1 /mnt/system/boot`
     - Mount usb: `$ mount /dev/sdb1 /mnt/usb`
     - examine:
         - `$ ls /mnt/system`
         - `$ls /mnt/usb`
     - Restore:
    
     ```bash
     $ rsync -aAXv --delete --exclude="lost+found" /mnt/usb/ /mnt/system
     ```
    
     - Check if the contents of `$ls /mnt/system` are restored.
     -Leave mount:
         - `$lsblk`, you may see that the MOUNTPOINT columns of sda1~sda4 have values. (uncertain)
         - Type the command `$ umount -R /mnt`
         - At this time, run `$ lsblk` again, and you may see that only the MOUNTPOINT column of sda2 has a value. (uncertain)
     - Shutdown `$ shutdown now`
     - Remove the iso and reopen arch.
     - The state of arch at this time is the state of the restore point.
     - Finish


# Install Nvidia 3D acceleration driver

reference document:
- [NVIDIA - ArchWiki](https://wiki.archlinux.org/index.php/NVIDIA)
- [Easiest way to Install Nvidia 3D Graphics acceleration driver on ArchLinux](https://computingforgeeks.com/easiest-way-to-install-nvidia-3d-graphics-acceleration-driver-on-archlinux/)


Before installing the driver, you must first install the graphics card on the host. (This article was tested with the graphics card GTX 1080)


Type the command to confirm:

```bash
$ lspci -k | grep -A 2 -E "(VGA|3D)"
```

The last line should look like this:

```bash
Kernel driver in use: nouveau
```

- If you don’t see the name of your graphics card, it means you haven’t installed it properly.
- If nouveau is displayed instead of nvidia, then you should have installed the nvidia driver, and you can skip this chapter.

[nouveau](https://wiki.archlinux.org/index.php/Nouveau) is nvidia universal graphics card driver.
But we don’t want it, because if we want to use cuda gpu hard solution acceleration operation,
The nvidia-driver system is required. And add the original default nouveau driver to the blacklist.
Fortunately, someone has sorted out the installation process.

Then get ready to enter the installation steps:
- System total package update. `$ sudo pacman -Syyu`
- Install nvidia driver. `$ sudo pacman -S nvidia nvidia-utils nvidia-settings xorg-server-devel opencl-nvidia`
- Check if nouveau has been blacklisted. `$ cat /usr/lib/modprobe.d/nvidia.conf`
     - Normally display `blacklist nouveau`
     - If not, please add the `blacklist nouveau` text to that file.
     - Supplement: Normally, after installing the nvidia driver, it will add nouveau to the blacklist by itself. And there is no need to do *nvidia-config* yourself to automatically generate the *xorg.conf* file.
- restart. `$reboot`
- Installed.

monitor:
- Monitor GPU status. `$nvidia-smi`
- Monitor GPU temperature. `$ nvidia-smi -q -d TEMPERATURE`

Check if Direct rendering is started and functioning properly:
- Install [glxinfo](https://aur.archlinux.org/packages/glxinfo/)
     - `$ git clone https://aur.archlinux.org/glxinfo.git`
     - `$ cd glxinfo`
     - `$ makepkg -s`
     - `$ sudo pacman -U glxinfo-8.4.0-1-x86_64.pkg.tar.xz`
- examine. `$ glxinfo | grep direct`.
     - The first line will say *direct rendering: Yes*
     - After the second line, check to see if there is any text similar to:
    
     ```bash
     GL_ARB_direct_state_access, GL_ARB_draw_buffers,
     GL_ARB_draw_indirect, GL_ARB_draw_instanced, GL_ARB_enhanced_layouts,
     GL_ARB_indirect_parameters, GL_ARB_instanced_arrays,
     GL_ARB_map_buffer_range, GL_ARB_multi_bind, GL_ARB_multi_draw_indirect,
     ```

#Install Firewall
- Refer to [Uncomplicated Firewall](https://wiki.archlinux.org/index.php/Uncomplicated_Firewall)
- Install:
     - `$ sudo pacman -S ufw`
     - `$ systemctl start ufw`
     - `$ systemctl enable ufw`
- Basic settings:
     - `$ sudo ufw default deny`
     - `$ sudo ufw allow from 192.168.0.0/24`
     - `$ sudo ufw allow Deluge`
     - `$ sudo ufw limit SSH`
- use:
     - Enable: `$ sudo ufw enable`
     - Close: `$ sudo ufw disable`
     - Status query: `$ sudo ufw status`
     - Command query: `$ ufw --help`

# Adjust the appearance of Xfce terminal
- After installing xfce, the default terminal is xfce. Of course you can change to gnome-terminal, xlterminal, etc.
- This article is mainly about xfce.
- Open terminal
- Click "Edit" -> "Preferences" on the menu, and then the terminal preferences window will appear.
- Click on the tab "Apperence":
     -Font area:
         - Adjust font and font size (use system font is unchecked). For example: monospace regular 13
         - Cell Spacing adjusts the spacing between the top, bottom, left and right of the font. For example: 1.10 x-width, 1.15 x-height
     -Background area:
         - Can use preset Solid
         - You can also use your own picture as the background
         - You can also use a somewhat transparent background. For example: opacity: 0.95
- Click on the tab "Colors":
     - "Presets" at the bottom:
         - You can choose some of the appearances it has adjusted. For example: Dark Pastels
- After setting it up like this, it should look much better than before.

# Set terminal shortcut keys
- Click Application -> "Settings" -> "Settings Manager" in the upper left corner
- Click on the tab "Application Shortcuts"
- Click "Add" below
- Type /usr/bin/xfce4-terminal and press OK
- Next it asks to set the shortcut key, please press the keyboard keys ctrl+alt+t
- This is set, press Close to close the keyboard setting window
- Finish

# Change desktop background
- You may find the mouse on the desktop pattern annoying (?)
- You can go to this website [Desktop background pictures](https://unsplash.com/search/photos/desktop-background) to download the desktop you want
- Then put the image into `/usr/share/backgrounds/xfce`
- Right click on the desktop and click "Desktop Settings"
- In the Background tab, you should be able to see the background image you just captured.
- Click it and press close to close it
- New desktop completed.

# Advanced Xfce appearance settings
- Requirements:
     - Install all xfce-related packages
     - `$ pacman -Sl | grep xfce`, install all the listed package names
     - Installation command `$ sudo pacman -S <pkg_name>`
- Please refer to the video [Customise XFCE desktop | arch linux](https://www.youtube.com/watch?v=M2jy5J3Y-vw)
- Replenish:
     - There is a tutorial on how to set up the network in the video, which requires the network device name.
       By default in arch, ifconfig cannot be used, and `$ip addr` is used instead. Or you can use `$ lspci -v`. Here we take the *ip addr* command as an example. After typing this command, you can see three names:
         - lo: locahost. Ignore it.
         - enp3s0: ethernet. If you are using a wired network, this is the name of the network device.
         - wlp4s1: Wireless network. If you are using a wireless network, this is the name of the network device.
        
     - After everything is installed, if you want to modify some commonly used built-in system shortcut keys, you can click on the "whisker menu" (blue round icon), search for "Window manager", and then click on the label "Keyboard". This list These are some commonly used shortcut keys. For example: "Show Desktop".

# Can I use something like Microsoft Office on Arch?
- The answer is yes.
- Install [libre-office](https://wiki.archlinux.org/index.php/LibreOffice). It can open ms-doc series files and save them in its format. The key point is **completely free**!!
- Type `$ pacman -Sl | grep libreoffice`, and there will be many packages, including libreoffice-still and libreoffice-fresh. Both are available. Just pick one and download it. The rest depends on the language. For Taiwanese Chinese, It's called zh-tw, so if you choose fresh, the final installation command is

     ```bash
     $ sudo pacman -S libreoffice-fresh-zh-tw
     ```

- Finish

# Watch hard drive usage
You can use the command: `$dh -h`.


# Add Network DNS
DNS is a service system used to convert URL strings into IP addresses. Its full name is Domain Name System. For example: http://www.google.com will be converted to 172.217.27.132 after passing through DNS.
There are many DNSs, you can refer to [this table](https://support.rackspace.com/how-to/changing-dns-settings-on-linux/). Or some companies will have their own DNS, for example: 192.168.0.200. Adding an extra stable DNS will prevent one day from the default DNS being broken and you not being able to access the Internet.

Add DNS steps:
- Open the /etc/resolv.conf file with sudo privileges:

```bash
$ sudo vim /etc/resolv.conf
```

- Add DNS

```
#Generated by NetworkManager
nameserver 192.168.0.200 # default one (Maybe Your Company's DNS)
nameserver 8.8.4.4 # This is what I added now. (google DNS)
```

- Save and exit
- Use the `ping` command to test connectivity to any URL.
- Finish.
