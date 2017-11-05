# linux-max98090
(Pre-compiled) Archlinux kernel for baytrail chromebooks with byt-max98090 sound.
Built from source files in AUR https://aur.archlinux.org/packages/linux-max98090/

# Add the repo to your /etc/pacman.conf

``` shell
[duffydack]
Server = https://github.com/duffydack/linux-max98090/releases/download/current/
```
# Add my gpg key, sign it, and install kernel
``` shell
sudo pacman-key -r 67DDC5FDAB2AEF18
sudo pacman-key --lsign-key 67DDC5FDAB2AEF18
sudo pacman -Syu ; sudo pacman -S linux-max98090 linux-max98090-headers
```

For those using Seabios RW Legacy/Boot Stub, Do yourself a favour and use the UEFI rom from https://mrchromebox.tech/#fwscript

# Issues
Still got the garbled/dalek distortion problem when using duplex (input+output).  Restarting pulseaudio temporarily fixes it.  Suck it up people, we've been left an old obsolete driver by the kernel devs.  Keep sending your thoughts and prayers though.
