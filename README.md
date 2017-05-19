# raspi_kernel
A collection of some ready for use Raspi kernels

Just a hopefully growning collection of ready to use kernels. The compiling and setup is taking a lot of time on a Raspbian and not everybody can make a cross compile setup. The things to do are usually very simple. 

Copy the file into your /tmp directory, enter it on console, terminal, ssh and:

```
sudo rm -r /boot/overlays/
sudo rm -r /lib/firmware/
cd /tmp
sudo tar xzf <KERNELFILE>.tgz -C /
sudo shutdown -r now
```
