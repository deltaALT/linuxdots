# linuxdots
(almost) all of my dotfiles for my EndeavourOS i3wm setup.

## Installation (W.I.P.)
I tried my best to explain it as simple as possible...
> [!IMPORTANT]
> This is a work in progress, which means it's NOT done, so please, do not follow this section yet (unless you really want to risk ending up with broken configs/incomplete stuff, since there are a lot of configs that I haven't included yet...)
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

Since Linux doesn't make files executable by default, we need to run some commands.

```cd into .config/i3blocks/scripts```

```cd .config/i3blocks/scripts```

To make the stuff on the bar appear (like on the picture below)
![image](https://github.com/deltaALT/linuxdots/assets/154239532/a35cfc34-ae4b-47a9-8fdb-423daff843fb)
Run the following commands, one by one:
cd into Volume

```cd volume```

and run this command:

```chmod +x volume```

Now go back a directory (```cd ..```)

And repeat the same with the other modules:

```cd battery```

```chmod +x battery```


```cd ..```


```cd wifi```

```chmod +x wifi```

Refresh i3 by pressing $mod + shift + r ($mod is the super/meta/"Windows" key by default)

Now you're done configuring i3 and everything :)

If you've done everything correctly, it should look like this:
![image](https://github.com/deltaALT/linuxdots/assets/154239532/abc3c62a-74c1-4edd-a9ab-2c995c2f6bb9)


Let me know if you like it and suggest stuff that I should improve (You can suggest stuff in the issues tab).

### Thanks/Credits

Thanks to:

[The Linux Cast](https://www.youtube.com/@TheLinuxCast), for helping me set i3 up (im a newbie)

The videos I used from him are [Things to Do After Installing i3 Windows Manager](https://www.youtube.com/watch?v=Jil4nqMw6ak) and [Customizing i3Blocks For the Ultimate Status Bar on i3WM](https://www.youtube.com/watch?v=Jil4nqMw6ak)



[fairyglade](https://github.com/fairyglade), for making [ly](https://github.com/fairyglade/ly)

[Dave Davenport](https://github.com/davatorium), for [rofi](https://github.com/davatorium/rofi)

[fish](https://fishshell.com/), a shell like bash or zsh, but better

and [IlanCosman](https://github.com/IlanCosman/), for making the fish prompt called [Tide](https://github.com/IlanCosman/tide)

