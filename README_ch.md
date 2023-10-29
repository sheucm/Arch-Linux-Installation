# 前言
這份檔案是給第一次要安裝Arch的人看的。   

Arch是什麼？

Arch是一個**什麼都要自己來安裝**的Linux作業系統，使用它的人被人稱之為"怪咖"，因為怪咖享受什麼都自己DIY的樂趣。

其實除了被人稱之為怪咖的好處(疑?)，Arch有其與其它Linux作業系統不同的地方，即：
- *所有Package皆是最新版本*
- *一個指令更新所有Package到最新*
- *環境最乾淨* (因為重頭到尾都是自己安裝的)

由於這三個大特點，使得Arch作業系統還是廣受一票人使用。


# 目錄
- [下載iso安裝檔](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E4%B8%8B%E8%BC%89iso%E5%AE%89%E8%A3%9D%E6%AA%94)
- [Arch參考文件](https://github.com/sheucm/Arch-Installation/blob/master/README.md#arch%E5%8F%83%E8%80%83%E6%96%87%E4%BB%B6)
- [安裝Arch Linux](https://github.com/sheucm/Arch-Installation/blob/master/README.md#arch%E5%8F%83%E8%80%83%E6%96%87%E4%BB%B6)
- [Add User](https://github.com/sheucm/Arch-Installation/blob/master/README.md#add-user)
- [Delete User](https://github.com/sheucm/Arch-Installation/blob/master/README.md#delete-user)
- [安裝package](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%AE%89%E8%A3%9Dpackage)
- [安裝Desktop GUI](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%AE%89%E8%A3%9Ddesktop-gui)
- [啟動或關閉Service](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%95%9F%E5%8B%95%E6%88%96%E9%97%9C%E9%96%89service)
- [系統總更新](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E7%B3%BB%E7%B5%B1%E7%B8%BD%E6%9B%B4%E6%96%B0)
- [~/.bashrc](https://github.com/sheucm/Arch-Installation/blob/master/README.md#bashrc)
- [VirtualBox共用資料夾設定](https://github.com/sheucm/Arch-Installation/blob/master/README.md#virtualbox%E5%85%B1%E7%94%A8%E8%B3%87%E6%96%99%E5%A4%BE%E8%A8%AD%E5%AE%9A)
- [VirtualBox雙向剪貼](https://github.com/sheucm/Arch-Installation/blob/master/README.md#virtualbox%E9%9B%99%E5%90%91%E5%89%AA%E8%B2%BC)
- [VirtualBox插入Usb](https://github.com/sheucm/Arch-Installation/blob/master/README.md#virtualbox%E6%8F%92%E5%85%A5usb)
- [安裝Chrome瀏覽器](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%AE%89%E8%A3%9Dchrome%E7%80%8F%E8%A6%BD%E5%99%A8)
- [其他常用安裝](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%85%B6%E5%AE%83%E5%B8%B8%E7%94%A8%E5%AE%89%E8%A3%9D)
- [安裝中文字體](https://github.com/sheucm/Arch-Installation/blob/master/README.md#install-chinese-fonts)
- [設定中文圖形化介面](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E8%A8%AD%E5%AE%9A%E5%9C%96%E5%BD%A2%E5%8C%96%E4%B8%AD%E6%96%87%E4%BB%8B%E9%9D%A2)
- [安裝中文輸入法](https://github.com/sheucm/Arch-Installation/blob/master/README.md#install-chinese-keyboard)
- [設定時間](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E8%A8%AD%E5%AE%9A%E6%99%82%E9%96%93)
- [設定音訊輸出與麥克風輸入](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E8%A8%AD%E5%AE%9A%E9%9F%B3%E8%A8%8A%E8%BC%B8%E5%87%BA%E8%88%87%E9%BA%A5%E5%85%8B%E9%A2%A8%E8%BC%B8%E5%85%A5)
- [安裝Usb介面](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%AE%89%E8%A3%9Dusb%E4%BB%8B%E9%9D%A2)
- [系統備份與還原](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%82%99%E4%BB%BD%E8%88%87%E9%82%84%E5%8E%9F)
- [安裝Nvidia 3D加速Driver](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%AE%89%E8%A3%9Dnvidia-3d-%E5%8A%A0%E9%80%9F-driver)
- [安裝防火牆](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%AE%89%E8%A3%9D%E9%98%B2%E7%81%AB%E7%89%86)
- [調整Xfce終端機外觀](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E8%AA%BF%E6%95%B4xfce-terminal%E5%A4%96%E8%A7%80)
- [設定終端機快捷鍵](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E8%A8%AD%E5%AE%9Aterminal%E5%BF%AB%E6%8D%B7%E9%8D%B5)
- [更換桌面背景](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E6%8F%9B%E8%83%8C%E6%99%AF)
- [進階Xfce外觀設定](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E9%80%B2%E9%9A%8Exfce%E5%A4%96%E8%A7%80%E8%A8%AD%E5%AE%9A)
- [Arch上可以用類似微軟Office嗎](https://github.com/sheucm/Arch-Installation/blob/master/README.md#arch%E4%B8%8A%E5%8F%AF%E4%BB%A5%E7%94%A8%E9%A1%9E%E4%BC%BC%E5%BE%AE%E8%BB%9Foffice%E5%97%8E)
- [觀看硬碟使用率](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E8%A7%80%E7%9C%8B%E7%A1%AC%E7%A2%9F%E4%BD%BF%E7%94%A8%E7%8E%87)
- [增加Network DNS](https://github.com/sheucm/Arch-Installation/blob/master/README.md#%E5%A2%9E%E5%8A%A0network-dns)

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
    - Last sector: +200M （至少200）
- 此時`p`，可以看到新的分割顯示在螢幕上。
- 再按`n`來新增swap用的分割區：
    - Partition Type: p
    - Partition Number: (default, press enter)
    - First sector: (default, press enter)
    - Last sector: +2G (大部分人建議為ram大小*150%，假設8G ram，swap就是設12G)
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
- 打上指令`lsblk`，這時候可以看到sda1、sda2、sda3、sda4。而且可以看到它們的容量分別是200M、2G、25G、剩餘容量。
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
    - 打上指令`grub-install --target=i386-pc /dev/sda` (注意：不是sda1，也不是sda2…)
    - 如果沒有error的話，再來產生grub config檔，打上指令`grub-mkconfig -o /boot/grub/grub.cfg`

### Part 3: 設定
- 設定root密碼，打上指令`passwd`，打上自己的密碼。
- 打上指令`nano /etc/locale.gen`，利用nano或vim編輯器來編輯locale.gen檔案，找到以下語系，將#拿掉，並儲存離開：
    - zh_TW.big5
    - zh_TW.utf8
    - en_US.iso88591
    - en_US.utf8
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

- 安裝：打上指令`pacman -S <package_name>`
- 查找：打上指令`pacman -Sl | grep <package_name>`
- 解除安裝：打上指令`pacman -Rs <package_name>`

若之前有用到ubuntu或其它linus系統，可以看[此table](https://wiki.archlinux.org/index.php/Pacman/Rosetta)可以更快學習pacman指令。

### 手動安裝

- 找到<package>的安裝repo
- clone到本地。打下指令`git clone <package-repo>`
- 進入該專案。打下指令`cd <package>`
- 製作安裝檔。打下指令`makepkg -s`。最後會在目錄下看到類似<package>.pkg.tar.xz的安裝檔。
- 安裝。打下指令`sudo pacman -U <package>.pkg.tar.xz`
- 安裝完成。
- 解除安裝：打上指令`pacman -Rsn <package_name>`

### 詳細有關於pacman
- `$ man pacman`
- `$ pacman --help`
- [Pacman - ArchWiki](https://wiki.archlinux.org/index.php/pacman)

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

# 系統總更新
更新所有使用從官方下載的套件。    
打上指令`$ sudo pacman -Syyu`。

# ~/.bashrc
`~/.bashrc`可以請系統開機後，就執行這檔案裡的script。
例如我想要在這裡設定alias、環境變數等。

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

# VirtualBox插入usb
- 下載[VirtualBox Extension Pack](https://www.virtualbox.org/wiki/Downloads)並安裝
- 重開virtualbox
- 對其虛擬機器按"設定值" -> "USB"，選擇"*USB 3.0 (xHCI) 控制器*"。(如果是usb2.0就選擇2.0的)
- 開機
- 在視窗上方的選單中，點選"裝置" -> "USB"，選擇自己插入的usb裝置。如此一來，就好比一個usb插入了這台虛擬機器。
- 檢查：打開終端機，打上指令`$ lsblk`，如果有看到類似sdb、sdc等，看一下容量大小是不是自己的usb大小，是的話就沒錯了。

# 安裝Chrome瀏覽器
- [參考文章](https://linuxhint.com/install-google-chrome-on-arch-linux/)
- Requirements: 要安裝git
- 安裝步驟：
    - `$ git clone https://aur.archlinux.org/google-chrome.git`
    - `$ cd google-chrome/`
    - `$ makepkg -s`
    - `$ sudo pacman -U google-chrome-63.0.3239.108-1-x86_64.pkg.tar.xz`
    - 安裝完畢，接下來按左上角的Application -> Internet -> Google Chrome，就能開始瀏覽器。

# 其它常用安裝
- git
- gedit (文字編輯器）
- wget （下載指令工具）
- unzip （zip解壓指令工具）
- firefox (火狐瀏覽器）
- [deepin-screenshot](https://www.archlinux.org/packages/?name=deepin-screenshot) (截圖GUI工具)
- [gpicview](https://www.archlinux.org/packages/community/x86_64/gpicview/) (圖片閱覽器）
- [net-tools](https://www.archlinux.org/packages/core/x86_64/net-tools/)(ifconfig指令)
- [nmap](https://www.archlinux.org/packages/extra/x86_64/nmap/)(nmap指令）
- [bind-tools](https://www.archlinux.org/packages/extra/x86_64/bind-tools/)(dig指令）

```bash
$ sudo pacman -S <package>
```

# Install Chinese Fonts
- [Arch Fonts](https://wiki.archlinux.org/index.php/fonts)
- **Download all following Chinese Fonts !** :
    - adobe-source-han-sans-cn-fonts
    - adobe-source-han-sans-tw-fonts
    - adobe-source-han-serif-cn-fonts
    - adobe-source-han-serif-tw-fonts
    - wqy-microhei
    - wqy-zenhei 
    - wqy-bitmapfont
    - ttf-arphic-ukai 
    - ttf-arphic-uming
    - opendesktop-fonts 
    - ttf-hannom 
    
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

# 設定圖形化中文介面
- 前言：如果覺得arch系統都是英文顯示，想要改成中文，可以參考這篇的設定
- 參考文章：
    - [Locale - ArchWiki](https://wiki.archlinux.org/index.php/locale)
    - [Localization/Traditional Chinese](https://wiki.archlinux.org/index.php/Localization/Traditional_Chinese_(%E6%AD%A3%E9%AB%94%E4%B8%AD%E6%96%87))
- Requirements: 要安裝中文字型。
- 設定中文介面步驟：
    - 打上指令 `$ locale -a`，檢查是否出現zh_TW.utf8。沒有的話，請在按照*參考文章*內的說明來產生中文語系。
    - 編輯/etc/locale.conf
    - 將它改成`LANG=zh_TW.UTF-8`
    - 重新開機

# Install Chinese Keyboard
- [Arch Fxitx](https://wiki.archlinux.org/index.php/Fcitx)
- Other Article: [Installing fcitx](http://echoyun.com/2017/10/02/installing-fcitx-chinese-ime-arch-linux/)
- Requirements: Chinese fonts should be installed.
- **Download traditional Chinese Keyboard**:
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

# 設定時間
如果發現右上角的時間是錯誤的，可以依下列指令說定時間：

```bash
# timedatectl set-time "yyyy-MM-dd hh:mm:ss"
＄ timedatectl set-time "2018-10-204 17:56:54"
```

參考[Arch Time](https://wiki.archlinux.org/index.php/time)


# 設定音訊輸出與麥克風輸入
- 參考文件
    - [Arch - Sound system](https://wiki.archlinux.org/index.php/sound_system)
    - [Arch - Advanced Linux Sound Architecture](https://wiki.archlinux.org/index.php/Advanced_Linux_Sound_Architecture#Unmuting_the_channels)
    - [Arch - Advanced Linux Sound Architecture/Troubleshooting](https://wiki.archlinux.org/index.php/Advanced_Linux_Sound_Architecture/Troubleshooting#Microphone)
- 說明：處理音訊是Alsa Linux Kernal，它是內建的不用安裝，那我們指需要安裝它的utils，且預設是靜音，在步驟中會說明怎麼關閉靜音。
- 步驟：
    - 安裝alsa utils: `$ sudo pacman -S alsa-utils`。此時就會有兩個utilities，分別是*alsamixer*和*amixer*。
    - 利用alsamixer來取消靜音：`$ alsamixer`
    - 截一下官方文件說明：
    
    ```
    The MM label below a channel indicates that the channel is muted, and 00 indicates that it is open.

    Scroll to the Master and PCM channels with the ← and → keys and unmute them by pressing the m key.

    Use the ↑ key to increase the volume and obtain a value of 0 dB gain. The gain can be found in the upper left next to the Item: field.
    ```
    
    - 對Master按m，然後按上下鍵來調整音量。
    - 對HeadPhone按m，然後按上下鍵來調整音量。
    - 對Front Mic和Front按m，然後按上下鍵來調整音量。
    - 對Rear Mic按m，然後按上下鍵來調整音量。
    - 按f4進入Capture標籤，對兩個Capture按下Space鍵，並使用上下鍵來調整收音量。
    - Input Source的地方 （有兩個）按上下鍵改成Front Mic
    - 按Esc離開設定
- 測試：
    - 喇叭聲音：到youtube測試
    - 麥克風聲音：[Microphone Test](https://www.onlinemictest.com/)
    
# 安裝usb介面
- 參考[Udisks - ArchWiki](https://wiki.archlinux.org/index.php/Udisks)
- Requirements: 已安裝Desktop GUI
- 步驟：
    - 下載[udisk2](https://www.archlinux.org/packages/?name=udisks2)：`$ sudo pacman -S udisks2`。
    - 打上指令`$ lsblk`，來看usb裝置是在哪個磁區編號。假設usb裝置是在/dev/sdb：
    - mount usb: 打上指令`$ udisksctl mount -b /dev/sdb1`
    - unmount usb: 打上指令`$ udisksctl unmount -b /dev/sdb1`
    - 打開File Manager，在最左邊的DEVICES區就能看到自己的usb裝置。
    - 完成。
    
補充：目前還不知道怎麼使它自動mount usb裝置的方法。
    
# 備份與還原
- 文件參考：[rsync - ArchWiki](https://wiki.archlinux.org/index.php/rsync)
- 影片教學參考：[Backup and Restore Your Linux System with rsync](https://www.youtube.com/watch?v=oS5uH0mzMTg) :100: 
- 事前準備：
    - [格式為Ext4的usb](http://www.eassos.com/how-to/how-to-format-a-flash-drive.php)。
    - 在arch上安裝[rsync](https://www.archlinux.org/packages/?name=rsync)：`＄ sudo pacman -S rsync`
- 備份步驟：
    - arch開機，並插入usb
    - `$ lsblk`，來看usb磁區(我的是/dev/sdb1)
    - mount usb，`$ udisksctl mount -b /dev/sdb1`
    - 備份測試：
    
    ```bash
    $ sudo rsync -aAXv --delete --dry-run \
    --exclude=/dev/* --exclude=/proc/* \
    --exclude=/sys/* --exclude=/tmp/* --exclude=/run/* --exclude=/mnt/* \
    --exclude=/media/* --exclude="swapfile" --exclude="lost+found" \
    --exclude=".cache" --exclude="Downloads" --exclude=".VirtualBoxVMs" \
    --exclude=".ecryptfs" \
    /source /destination
    ```
    
    - 解釋備份測試指令：
        - /source為要備份的根目錄：取代為`/`。
        - /destination為備份到的地方：取代為`/run/media/eric/my_usb`
        - --dry-run。表示測試階段，還未真的寫入usb。測試階段，在console會印出要備份的檔案，可以在最後面加上`>> log.txt`，來看要備份的檔案是否有誤。
        - 其它參數的解釋，可以參考影片教學。
    - 真正備份到usb：確定列出備份的清單沒問題，就將*--dry-run*拿掉開始吧!
    - 打開usb資料夾，檢查是否都有備份進去。
    - unmount usb: `$ udisksctl unmount -b /dev/sdb1`。
    
- 還原步驟：
    - 重開機，安裝arch iso，並插入usb。
    - 開機後，畫面會停在iso command line，打上`$ ls`，應該只會看到install.txt。
    - 創兩個資料夾：`$ mkdir /mnt/system /mnt/usb`
    - `$ lsblk`，檢查是否存在usb，並看一下各磁區編號。例：
        - boot: /dev/sda1
        - root: /dev/sda3
        - home: /dev/sda4
        - usb: /dev/sdb1
    - Mount system： 
        - `$ mount /dev/sda3 /mnt/system`
        - `$ mount /dev/sda4 /mnt/system/home`
        - `$ mount /dev/sda1 /mnt/system/boot`
    - Mount usb： `$ mount /dev/sdb1 /mnt/usb`
    - 檢查：
        - `$ ls /mnt/system`
        - `$ ls /mnt/usb`
    - 還原：
    
    ```bash
    $ rsync -aAXv --delete --exclude="lost+found" /mnt/usb/ /mnt/system
    ```
    
    - 檢查 `$ ls /mnt/system` 內容是否還原到。
    - 離開mount：
        - `$ lsblk`，可能會看到sda1~sda4的MOUNTPOINT欄都有值。 (不確定)
        - 打上指令`$ umount -R /mnt`
        - 此時再 `$ lsblk` 一次，可能會看到只有sda2的MOUNTPOINT欄有值。 (不確定)
    - 關機 `$ shutdown now`
    - 移除iso，並重開arch。
    - 此時arch的狀態，便是還原點的狀態。
    - 完成


# 安裝Nvidia 3D 加速 Driver

參考文件：
- [NVIDIA - ArchWiki](https://wiki.archlinux.org/index.php/NVIDIA)
- [Easiest way to Install Nvidia 3D Graphics acceleration driver on ArchLinux](https://computingforgeeks.com/easiest-way-to-install-nvidia-3d-graphics-acceleration-driver-on-archlinux/)


安裝驅動前，要先將顯卡裝上主機上。（本篇是以顯示卡GTX 1080測試）


打上指令來確定一下：

```bash
$ lspci -k | grep -A 2 -E "(VGA|3D)"
```

最後一行應該會顯示像這樣：

```bash
Kernel driver in use: nouveau
```

- 如果沒看到自己顯卡的名字，表示你沒裝好。
- 如果不是顯示nouveau，而是nvidia，那你應該已經安裝過nvidia驅動了，那本章內容就可以跳過。

[nouveau](https://wiki.archlinux.org/index.php/Nouveau)是nvidia通用顯卡驅動。
但是我們不要它，因為如果要用到cuda gpu硬解加速運算的話，
要用到nvidia-driver系統的。並且要將原本預設的nouveau driver加入黑名單。
幸好已經有人整理出安裝流程。

那開始準備進入安裝步驟：
- 系統總套件更新。`$ sudo pacman -Syyu`
- 安裝nvidia驅動。`$ sudo pacman -S nvidia nvidia-utils nvidia-settings xorg-server-devel opencl-nvidia`
- 檢查nouveau是否已經被加入黑名單。`$ cat /usr/lib/modprobe.d/nvidia.conf`
    - 正常要顯示`blacklist nouveau`
    - 如果沒有的話，請將`blacklist nouveau`文字加入到那個檔案。
    - 補充：正常來說，安裝nvidia驅動後，它會自己將nouveau加入黑名單。並且也不用自己做*nvidia-config*來自動產生*xorg.conf*檔案。
- 重新開機。`$ reboot`
- 安裝完畢。

監控：
- 監控GPU狀態。`$ nvidia-smi`
- 監空GPU溫度。`$ nvidia-smi -q -d TEMPERATURE`

檢查Direct rendering是否啟動且運作正常：
- 安裝[glxinfo](https://aur.archlinux.org/packages/glxinfo/)
    - `$ git clone https://aur.archlinux.org/glxinfo.git`
    - `$ cd glxinfo`
    - `$ makepkg -s`
    - `$ sudo pacman -U glxinfo-8.4.0-1-x86_64.pkg.tar.xz`
- 檢查。`$ glxinfo | grep direct`。
    - 第一行會顯示*direct rendering: Yes*
    - 第二行以後，檢查看看是否有類似以下文字：
    
    ```bash
    GL_ARB_direct_state_access, GL_ARB_draw_buffers, 
    GL_ARB_draw_indirect, GL_ARB_draw_instanced, GL_ARB_enhanced_layouts, 
    GL_ARB_indirect_parameters, GL_ARB_instanced_arrays, 
    GL_ARB_map_buffer_range, GL_ARB_multi_bind, GL_ARB_multi_draw_indirect, 
    ```

# 安裝防火牆
- 參考[Uncomplicated Firewall](https://wiki.archlinux.org/index.php/Uncomplicated_Firewall)
- 安裝：
    - `$ sudo pacman -S ufw`
    - `$ systemctl start ufw`
    - `$ systemctl enable ufw`
- 基本設定：
    - `$ sudo ufw default deny`
    - `$ sudo ufw allow from 192.168.0.0/24`
    - `$ sudo ufw allow Deluge`
    - `$ sudo ufw limit SSH`
- 使用：
    - 開啟：`$ sudo ufw enable`
    - 關閉：`$ sudo ufw disable`
    - 狀況查詢：`$ sudo ufw status`
    - 指令查詢：`$ ufw --help`

# 調整Xfce Terminal外觀
- 裝好xfce，預設的terminal就是xfce的。當然你可以換成gnome-terminal、xlterminal等。
- 這篇以xfce為主。
- 打開terminal
- 按menu上的"Edit" -> "Preferences"，之後會出現terminal preferences的視窗
- 點開標籤"Apperence"：
    - Font區：
        - 調整字型、字體大小 （use system font不打勾）。例如：monospace regular 13
        - Cell Spacing調整字體之上下左右間距。例如：1.10 x-width, 1.15 x-height
    - Background區：
        - 可以用預設的Solid
        - 也可以用自己的圖當背景
        - 也可以用有點透明的背景。例如：opacity: 0.95
- 點開標籤"Colors"：
    - 最底下"Presets":
        - 可以選一些它調過的外觀。例如：Dark Pastels
- 這樣設定完應該比原本好看多了

# 設定terminal快捷鍵
- 點開左上角的Application -〉 "Settings" -> "Settings Manager"
- 點開標籤"Application Shortcuts"
- 按底下的"Add"
- 打上/usr/bin/xfce4-terminal，按OK
- 再來它要求要設定快捷鍵，請按鍵盤按鍵ctrl+alt+t
- 這樣就設定好了，按Close關閉keyboard設定視窗
- 完成

# 換背景
- 可能會覺得桌面圖案那隻老鼠看得很煩（？）
- 可以到這網站[Desktop background pictures](https://unsplash.com/search/photos/desktop-background)來下載所想要的桌面
- 再將圖片放到`/usr/share/backgrounds/xfce`
- 對桌面點右鍵，點"Desktop Settings"
- 在Background標籤中，應該就能看到剛抓下來的背景圖
- 點它，按close關閉
- 新桌面完成。

# 進階xfce外觀設定
- Requirements:
    - 將所有有關xfce的套件全裝
    - `$ pacman -Sl | grep xfce`，所列出來的套件名稱都安裝
    - 安裝指令`$ sudo pacman -S <pkg_name>`
- 請參考影片[Customise XFCE desktop | arch linux](https://www.youtube.com/watch?v=M2jy5J3Y-vw)
- 補充：
    - 影片裡面有教學如何設定network，需要network device名稱。   
      在arch中預設是不能使用ifconfig，以`$ ip addr`取代之。或是可以使用`$ lspci -v`也可以。這裡以*ip addr*指令為例。打上此指令，可以看到三個名稱：
        - lo： locahost。這不用理它。
        - enp3s0： ethernet。如果你是用有線網路，network device就是此名稱。
        - wlp4s1： 無線網路。如果你是用無線網路，network device就是此名稱。
        
    - 全部安裝完後，如果要修改一些常用的內建系統快捷鍵，可以點開"whisker menu"（藍色圓形icon)，搜尋打上"Window manager"，然後點開標籤"Keyboard"，此清單都是一些常用的快捷鍵。例如："Show Desktop"。

# Arch上可以用類似微軟Office嗎？
- 答案是可以的。
- 安裝[libre-office](https://wiki.archlinux.org/index.php/LibreOffice)。它可以開啟ms-doc系列的文件，也可以存成其格式，重點是**完全免費**!!
- 打上`$ pacman -Sl | grep libreoffice`，就會出現很多套件，有libreoffice-still和libreoffice-fresh，兩種都可以，挑一個下載就好，剩下就是看語系，以台灣中文來說，叫作zh-tw，所以如果挑fresh的話，最終安裝指令是

    ```bash
    $ sudo pacman -S libreoffice-fresh-zh-tw
    ```

- 完成

# 觀看硬碟使用率
可以使用指令： `$dh -h`。


# 增加Network DNS
DNS是用來轉換網址字串成ip的一個服務系統，全名是Domain Name System。例如：http://www.google.com經過DNS後，會轉成172.217.27.132。   
那DNS有很多，可以參考[這篇表格](https://support.rackspace.com/how-to/changing-dns-settings-on-linux/)。或像是有些公司它們會有自己的DNS，例如：192.168.0.200。多增加一個穩定的DNS，才不會哪一天，預設的DNS壞掉了，你就不能上網了。

增加DNS步驟：
- 使用sudo權限打開/etc/resolv.conf 檔案：

```bash
＄ sudo vim /etc/resolv.conf
```

- 增加DNS

```
# Generated by NetworkManager
nameserver 192.168.0.200  # default one (Maybe Your Company's DNS)
nameserver 8.8.4.4        # This is what I added now. (google DNS)
```

- 儲存離開
- 使用`ping`指令對任何網址測試是否連得到。
- 完成。
