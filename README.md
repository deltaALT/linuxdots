# linuxdots
(almost) all of my dotfiles for my EndeavourOS i3wm setup.

## Installation (W.I.P.)

> [!IMPORTANT]
> This is a work in progress, so please, do not follow this section yet (unless you really want to risk ending up with broken configs/incomplete stuff...)
> You must enable "Show hidden files" in your file manager. Otherwise, the ``.config`` folder that you've cloned won't show up there.

> [!CAUTION]
> Be careful when installing the [GRUB](https://www.gnu.org/software/grub/) theme,
as you might break the bootloader, resulting in an unbootable system.


> If there will ever be an installation script, then it'll be supported for Arch-based distros **only**. Do **not** attempt to run the script on Debian or Ubuntu-based distros.

First, you'll want to install some dependencies. To install them, simply run:

```sudo pacman -Syu fish git i3 konsole ly neofetch nitrogen rofi scrot wlogout``` 

After that, reboot the system. (otherwise if you log in to i3, it will be kinda broken, atleast for me.)

### Installing ly (the display manager)

[ly](https://github.com/fairyglade/ly) is the display manager you'll need to be able to log in to i3 ([sddm](https://github.com/sddm/sddm) doesn't work with i3)

To use ly as the default display manager, run:

```sudo systemctl enable ly.service```

After rebooting, you can log in to i3.

### Configuring i3 and everything else

After logging to i3, you'll be met with a black screen with a thin bar on the bottom. That's normal.

Clone this repository:

```git clone https://github.com/deltaALT/linuxdots.git```

Now cd into it and copy the contents of the folder to your home folder
```cd linuxdots/```
```rsync -a .config ~```
Refresh i3 by pressing $mod + shift + r ($mod is the super/meta/"Windows" key by default)

Now you're done configuring i3 and everything :)

Let me know if you like it and suggest stuff that I should improve (You can suggest stuff in the issues tab).

