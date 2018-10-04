# 前言
這分檔案是給第一次要安裝Arch的人看的。

# 下載iso安裝檔
- 請到[此官網](https://www.archlinux.org/download/)下載torrent檔，利用torrent軟體下載iso檔。
- 將iso檔燒成光碟或usb，將光碟機或usb成為開機第一優先順序

# Arch參考文件
- [Frequently asked questions](https://wiki.archlinux.org/index.php/Frequently_asked_questions)
- [Installation guide](https://wiki.archlinux.org/index.php/Installation_guide)
- [Users and groups](https://wiki.archlinux.org/index.php/users_and_groups)
- [General recommendations](https://wiki.archlinux.org/index.php/General_recommendations)
- [pacman](https://wiki.archlinux.org/index.php/pacman)

# 安裝Arch Linus

安裝詳細教學，可以觀看[**此影片**](https://www.youtube.com/watch?v=4PBqpX0_UOc):100:       


以下用文字記錄安裝流程：
- 開機後，會發現進入一個選單，請選擇**Boot Arch Linux**的選單。
- 之後會以root身份進入command line模式

### Part 0: 前置設定
- 觀看一下目前disk的狀況，請下指令 `lsblk`。會看到你硬碟的狀況，通常會看到sda或sdb的字眼。設假這篇要安裝的磁碟叫sda。
- 檢查硬碟是否為UEFI (不用了解這是什麼)，如果為UEFI的話，不適用此篇。
    怎麼檢查？打上指令`ls /sys/fireware/efi/efivars`，如果跑出No such file or directory，那就對了。反之，如果跑出很多檔案，那你的碟就是UEFI，不適用此篇教學。
- 檢查是否有網路。打上指令`ping www.google.com`。
- 設定時間：打上指令`timedatectl set-ntp true`

### Part 1: 分割hard drive
- 打上指令`fdisk /dev/sda`準備分割 (若你的是sdb就改sdb)。
- 此時可以輸入m來看說明。(簡單操作說明：`p`就是印出磁碟狀況；`d`就是刪除現有磁碟分割；`n`新增分割；`w`將修改確定寫入磁碟)
- 先按`n`來新增boot用的分割區：
    - Partition Type: p
    - Partition Number: (default, press enter)
    - First sector: (default, press enter)
    - Last sector: +200M
- 此時`p`，可以看到新的分割顯示在螢幕上。
- 再按`n`來新增swap用的分割區：
    - Partition Type: p
    - Partition Number: (default, press enter)
    - First sector: (default, press enter)
    - Last sector: +1G (大部分人建議磁碟容量*10%)
- 再按`n`來新增root用的分割區：
    - Partition Type: p
    - Partition Number: (default, press enter)
    - First sector: (default, press enter)
    - Last sector: +25G (建議至少25G)
- 再按`n`來新增home用的分割區：
    - Partition Type: p
    - Partition Number: (default, press enter)
    - First sector: (default, press enter)
    - Last sector: (default, press enter)
- 此時，按下`p`可以看到已完美分割好的分割區。
- 按下`w`來儲存所有變更。注意：這將永遠抹除磁碟資料。
- 打上指令`lsblk`，這時候可以看到sda1、sda2、sda3、sda4。而且可以看到它們的容量分別是200M、1G、25G、剩餘容量。
- 再來要對sda1、sda3、sda4安裝file system：
    - 打上指令`mkfs.ext4 /dev/sda1`
    - 打上指令`mkfs.ext4 /dev/sda3`
    - 打上指令`mkfs.ext4 /dev/sda4`
- 再來要對sda2標記為swap：
    - 打上指令`mkswap /dev/sda2`
    - 打上指令`swapon /dev/sda2`
- 這時候打上指令`lsblk`可以看到sda2的MOUNTPOINT欄有[SWAP]標記。
- 再來對要sda1、sda3、sda4進行mount
- 先對sda3 (root) 進行mount動作，打上指令`mount /dev/sda3 /mnt`。
- 打上指令`ls /mnt`，可以發現有lost+found檔案。
- 這時打上指令`lsblk`，可以發現sda3的MOUNTPOINT欄有/mnt。
- 創建home和boot資料夾：
    - 打上指令`mkdir /mnt/home`
    - 打上指令`mkdir /mnt/boot`
- 為sda1(boot)、sda4(home)進行mount動作：
    - 打上指令`mount /dev/sda1 /mnt/boot`
    - 打上指令`mount /dev/sda4 /mnt/home`
- 這時打上指令`lsblk`，可以看到sda1和sda4的MOUNTPOINT欄分別是/mnt/boot和/mnt/home。


### Part 2: 安裝系統
- 安裝Arch Linux：
    - 打上指令`pacstrap /mnt base base-devel vim`，順便安裝vim。(要等一段時間)
- 產生fstab，它的用途在於開機時，能自動選到正確的位置啟動Arch作業系統。
    - 我們將用genfstab指令，可以直接打上指令`genfstab`會有說明用法。
    - 打上指令`genfstab /mnt`，可以看到四個sda分割區對應的資料，但我們要用uuid，比較安全，所以…
    - 打上指令`genfstab -U /mnt`，加上-U，可以看到輸出換成uuid了。
    - 將它輸出到/mnt/etc/fstab檔案，打上指令`genfstab -U /mnt >> /mnt/etc/fstab`。
    - 打上指令`vim /mnt/etc/fstab`，內容應該有sda1~4，四筆資料。
- 接下來要真正進入Arch系統：打上指令`arch-chroot /mnt`
- 這時候，從ISO系統進入到真正DISK安裝完的ARCH系統。所以可以打上指令`vim /etc/fstab`觀看到剛剛建立的fstab檔案。

### part 3: 安裝網路
- 打上指令`pacman -S networkmanager`
- 啟動network manager。打上指令`systemctl enable NetworkManager`
- 安裝grub，它是一種bootloader。
    - 打上指令`pacman -S grub`
    - 打上指令`grub-install -target=i386-pc /dev/sda` (注意：不是sda1，也不是sda2…)
    - 如果沒有error的話，再來產生grub config檔，打上指令`grub-mkconfig -o /boot/grub/grub.cfg`

### Part 3: 設定
- 設定root密碼，打上指令`passwd`，打上自己的密碼。
- 打上指令`nano /etc/locale.gen`，利用nano或vim編輯器來編輯locale.gen檔案，按page-down鍵到最下面，找到zh_TW，將#拿掉。然後儲存離開。
- 打上指令`locale-gen`，來產生locale。
- 移動到`/usr/share/zoneinfo/`目錄，可以看到很多時區。以台灣來說是屬於`Asia/Taipei`。所以請打上指令`ln -sf /usr/share/zoneinfo/Asia/Taipei /etc/localtime`。


- 打上指令`vim /etc/hostname`，進入該檔案打上自己的hostname(自己取)，儲存離開。
- 打上指令`exit`，離開磁碟Linux系統
- 離開mount，打上指令`umount -R /mnt`
- 打上指令`lsblk`，可以看到sda1~4的MOUNTPOINT，只有sda2是寫SWAP，其它都是空白了。
- 打上指令`shutdown now`，關機。
- 拔掉安裝檔 (iso)，並且重開機。
- 進入grub選擇，選擇預設*Arch Linux*。就算不選擇，過幾秒就會自己進入。
- login打上root，密碼打上剛剛設的。
- 安裝完成。

# Add User
詳細資料可以參考[Arch Wiki - Users and Groups](https://wiki.archlinux.org/index.php/users_and_groups) :thumbsup: 

以下簡單創造一個新的User叫eric為例，並且可以使用sudo權限：
- 以root帳號登入。
- 可以先打上指令`passwd -Sa`，查看一下目前的user有哪些，應該會看到root。
- 打上指令`useradd --create-home -G wheel eric`，來創造一個使用者叫eric，並且有自己的家目錄，wheel表示有sudo權限。
- 打上指令`passwd eric`，來設定此使用者的密碼。
- 打上指令`visudo`，找到*root ALL=(ALL) ALL*這行代碼。在它下面加上`eric ALL=(ALL) ALL`(或是將下面的`#%wheel ALL=(ALL) ALL`的#拿掉，也可以)，再儲存離開。若不會使用vi編輯器者，請自行google。
- 打上指令`exit`，離開root，以eric帳號登入。
- 打上指令`pwd`，看看是否處於`/home/eric`目錄下。
- 打上指令`sudo -s`，測試是否成功擁有root權限。
- 完成。

# Delete User
如果要刪除使用者，可以使用`userdel`指令，以上一節eric使用者為例，如果要刪除eric：
- 以root登入。
- 輸入指令`userdel -r eric`，來刪除eric使用者。`-r`表示刪除包括家目錄、mail。
- 輸入指令`passwd -Sa`，應該看不到eric了。
- 輸入指令`ls /home`，應該看不到eric的資料夾了。
- 完成。


# 安裝package

### 官方下載

可以上[這arch網站](https://www.archlinux.org/packages/)查找自己想要的package是否官方有提供。有的話就可以：

- 安裝：打上指令`pacman -S <repo>:<package_name>`
- 查找：打上指令`pacman -Sl | grep <package_name>`

若之前有用到ubuntu或其它linus系統，可以看[此table](https://wiki.archlinux.org/index.php/Pacman/Rosetta)可以更快學習pacman指令。

### 手動安裝

- 找到<package>的安裝repo
- clone到本地。打下指令`git clone <package-repo>`
- 進入該專案。打下指令`cd <package>`
- 製作安裝檔。打下指令`makepkg -s`。最後會在目錄下看到類似<package>.pkg.tar.xz的安裝檔。
- 安裝。打下指令`sudo pacman -U <package>.pkg.tar.xz`
- 安裝完成。

# 安裝Desktop GUI
- 可以參考此影片：[After a Minimal Linux Install: Graphical Envionment and Users](https://www.youtube.com/watch?v=nSHOb8YU9Gw) :thumbsup\_tone3: 
- 安裝x.org。打上指令`pacman -S xorg-server xorg-xinit`。不管你是要裝Desktop或是Window，都要安裝xorg。
- 安裝xfce Desktop。打上指令`pacman -S xfce4`
- 設定**.xinitrc**檔案。將`exec xfce4-session`這行加入到`~/.xinitrc`檔案裡。
- 打上指令`startx`，進入GUI介面。
- 安裝display manager (簡稱dm)：
    - 打上指令`sudo pacman -S lightdm lightdm-gtk-greeter`
    - 打上指令`sudo systemctl enable ligthdm.service`，告訴系統每次開機後就啟動lightdm。

    補充：dm是當你進入login時，會有GUI介面可以選擇登入的使用者，可以在DM介面打上登入密碼。如果不想要安裝dm也可以，就是每次開機會先進入tty模式login後，再打上startx指令，就可以進入GUI介面。

# 啟動或關閉service
- 啟動：打上指令`sudo systemctl start <service>`
- 關閉：打上指令`sudo systemctl stop <service>`

# .profile或.bash_profile
`~/.profile`或`~/.bash_profile`有點像ubuntu的`~/.bashrc`，可以請系統開機後，就執行這檔案裡的script。

# VirtualBox共用資料夾設定
- 先在本機上新增一個要共用的資料夾。例如: `D:\VirtualBoxShareArch`
- arch開機，在視窗索引列中按下**裝置** -> **共用資料夾** -> **共用資料夾設定**，按右邊+新增資料夾，選取D:\VirtualBoxShareArch資料夾，勾選"自動掛載"和"設為永久"選項，然後按確定。
- 安裝virtualbox guest addition:
    - 打上指令`sudo pacman -Sl | grep virtualbox`，可以看到有相關的套件可以安裝。
    - 打上指令`sudo pacman -S virtualbox-guest-modules-arch`
    - 打上指令`sudo pacman -S virtualbox-guest-utils`
- 重新開機。
- 為arch新增一個共用資料夾。例如: `/home/eric/Desktop/share`
- 打上指令`sudo mount -t vboxsf VirtualBoxShareArch /home/eric/Desktop/share`。此時Arch上的share資料夾，就與本機上的VirtualBoxShareArch資料夾是共用的。
- 完成

# VirtualBox雙向剪貼
- 必須完成 **VirtualBox共用資料夾設定** 步驟
- 關機狀態
- 點其機器"設定值" -> 一般 -> 進階：
    - 共用剪貼簿：雙向
    - 拖放：雙向
- 完成

# 其它安裝
- git安裝：打入指令`sudo pacman -S git`
- [chrome瀏覽器安裝](https://linuxhint.com/install-google-chrome-on-arch-linux/)
- 文字編輯器安裝gedit：打入指令`sudo pacman -S gedit`


# Install Chinese Fonts
- [Arch Fonts](https://wiki.archlinux.org/index.php/fonts)
- **Download all Chinese Fonts !** The following is for example:
    - download *adobe-source-han-sans-tw-fonts*: `$ sudo pacman -S adobe-source-han-sans-tw-fonts`
    - If the package is not on arch repo, like *noto-fonts-tc* (there is AUR words after those kind of fonts):
        - Click that link. In new page, copy the *Git Clone URL*
        - clone it. `$ git clone https://aur.archlinux.org/noto-fonts-tc.git`
        - `$ cd noto-fonts-tc`
        - `makepkg -s`
        - `sudo pacman -U noto-fonts-tc-20150617-1-any.pkg.tar.xz`
        - Reboot your arch. `$ reboot`
        - Finished Installing that ttf !
    
# Install Chinese Keyboard
- [Arch Fxitx](https://wiki.archlinux.org/index.php/Fcitx)
- Other Article: [Installing fcitx](http://echoyun.com/2017/10/02/installing-fcitx-chinese-ime-arch-linux/)
- Requirements: Chinese fonts should be installed.
- **Download traditional Keyboard**:
    - fxitx
    - fcitx-chewing 
    - fcitx-table-extra （if you want to use [Boshiamy](https://en.wikipedia.org/wiki/Boshiamy_method))
    - fcitx-im  
    - fcitx-configtool
    
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
- Add your favorite input methods
- Done. (終於可以打中文了！！）

