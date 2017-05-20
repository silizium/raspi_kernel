# raspi_kernel
A collection of some ready for use Raspi real-time kernels. 

Just a hopefully growning collection of ready to use kernels. The compiling and setup is taking a lot of time on a Raspbian and not everybody can make a cross compile setup. The things to do are usually very simple. 

Copy the file into your /tmp directory, enter it on console, terminal, ssh and:

```
sudo rm -r /boot/overlays/ /lib/firmware
cd /tmp
tar xzf <KERNELFILE>.tgz
sudo cp -rd lib /
sudo cp -rd boot /
sudo shutdown -r now
```
If you are using rpi-update, execute the rpi-update *before* you insert the new Kernel, because it would be overwritten.

Sources:

RT patch from here
https://www.kernel.org/pub/linux/kernel/projects/rt/

Kernel from here: 
git clone https://github.com/raspberrypi/linux.git

Process described here:
http://www.frank-durr.de/?p=203

I just compiled the Kernel (takes about a week on a Raspi 1B) and I do provide the result here. Do with it, what you like but don't blame me if it is not working or you are wrecking everything or so. 

I compiled that thing with a cross compiling process with a gcc 6.3 or did I use the toolchain? Whatever. It works for me. 
```
11305> arm-linux-gnueabihf-gcc --version                                                                                    ⏎
arm-linux-gnueabihf-gcc (Ubuntu/Linaro 6.3.0-12ubuntu2) 6.3.0 20170406
Copyright (C) 2016 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```
