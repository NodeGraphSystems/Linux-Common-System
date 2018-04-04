# Linux-Common-System
Making Linux based OS with custom Kernel Modules Can be sued for Embedded Applications for customized Hardware and Gateway IOT technologies. https://en.wikipedia.org/wiki/List_of_build_automation_software Building with Yocto, Buildroot, OpenWRT, Cmake, Make -BitBake, a Python-based tool with the special focus of distributions and packages for embedded Linux cross-compilation -Buildout, a Python-based build system for creating, assembling and deploying applications from multiple parts


Yocto steps:

cd build


Build images:

MACHINE=intel-x86-32 bitbake -c menuconfig virtual/kernel  #for building kernal with menuconfig check

MACHINE=intel-x86-32 bitbake -k rootfs-image

images in            ./tmp/deploy/images


code built from repos, binaries, source files result will be in  ./tmp/work/


Build SDK :

SDKMACHINE=x86_64 MACHINE=intel-x86-32 bitbake -k universal-dev -c populate_sdk

SDK folder               ./tmp/deploy/sdk


OpenWrt Buildroot:

your target device, like /bin, /tmp/, /usr, etc.

images at the “topdir/output/build/images”

conventional method like “tftp” to flash images into the device.


make list-defconfigs  # Displays list of boards within defconfig

./Run.sh setup

./Run.sh help

source ~/.bash_profile

make menuconfig # menuconfig check
