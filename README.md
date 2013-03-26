linux-mbp62
===========

Patched kernel for the MacBook Pro 6,2.  

The kernel contains the patches required to allow switching to the integrated Intel GPU with a working screen and framebuffer. As of 2013-03-10, the kernels shipped with Arch Linux, as well as the AUR linux-mainline package
do not have these patches applied, and will result in a black screen if you attempt to switch GPUs.

This package uses the linux-mainline [AUR package](https://aur.archlinux.org/packages/linux-mainline/) as a base, with Seth Forshee's [vga_switcheroo patch](http://lists.freedesktop.org/archives/dri-devel/2012-September/027528.html).

# Arch Linux Users #

Either grab the package from the prebuilt folder and install with `# pacman -S linux-mainline-3.9rc4-1-x86_64.pkg.tar.xz` or build the package yourself using `makepkg -s`.

# <Insert Distro Here> Users #

If you're fine compiling your own kernel, get the 3.9rc4 tarball from the usual sources and apply `mbp62.patch`.  
If you're feeling lazy, you could extract the kernel, modules, and headers from the `*.pkg.tar.xz` and stick them in the right places.  
If you're a linux newbie, I'd suggest asking for help on your distribution's forums/subreddit.
