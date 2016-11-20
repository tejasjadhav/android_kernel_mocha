# Xiaomi Mi Pad Kernel source

---

### Credits
[MIUI team](https://github.com/MiCode/) - Finally released the kernel source for Mi Pad.

[Harrynowl](https://github.com/harrynowl/) - Thanks for helping me getting the basic built start, and also the `.gitignore`.

---

## Download
* Download or clone the latest toolchain from <http://github.com/Christopher83/arm-cortex_a15-linux-gnueabihf-linaro_4.9> in a directory *(For example, `/home/<your_name>/toolchain/linaro-4.9/`)*.
* Download or clone the kernel source in a directory *(For example, `/home/<your_name>/kernel/mocha/`)*.
* Install some required OS packages.
```bash
sudo apt-get install build-essential
```

## Build
* Open terminal in the `kernel/mocha` directory.
* Run following commands,
```bash
make mocha_user_defconfig ARCH=arm
make ARCH=arm CROSS_COMPILER=/home/<your_name>/toolchain/linaro-4.9/bin/arm-cortex_a15-linux-gnueabihf-
```
* Once build is complete, you can find the `zImage` in `arch/arm/boot/` directory and `tegra124-mocha.dtb` in `arch/arm/boot/dts/` directory.
