# Set up RTEMS ARM BSP on Host OS

#### Note: Make sure you have `python 2.7` (devloper version), `python 3` and `pax` package installed on your system.

---

## RSB
### Setup RSB
~~~~
$ cd
$ mkdir -p development/rtems && cd development/rtems
$ git clone git://git.rtems.org/rtems-source-builder.git rsb
$ cd rsb
$ ./source-builder/sb-check
$ cd rtems
$ ../source-builder/sb-set-builder --list-bsets
~~~~

### Build Toolchain for ARM using RSB
~~~~
$ ../source-builder/sb-set-builder --prefix=/home/eshan/development/rtems/6 6/rtems-arm
~~~~

---

## Build RTEMS using Toolchain
~~~~
$ cd
$ cd development/rtems
$ mkdir kernel
$ cd kernel
~~~~
~~~~
$ git clone git://git.rtems.org/rtems.git rtems
~~~~
### Bootstrapping
~~~~
$ export PATH=$HOME/development/rtems/5/bin:$PATH 
$ cd rtems
$ ./bootstrap -c && ./rtems-bootstrap
~~~~
### Building a BSP
~~~~
$ cd ..
$ mkdir xilinx_zynq_a9_qemu
$ cd xilinx_zynq_a9_qemu
~~~~
~~~~
$ /home/eshan/development/rtems/kernel/rtems/configure --prefix=/home/eshan/development/rtems/5 --enable-maintainer-mode --target=arm-rtems5 --enable-rtemsbsp=xilinx_zynq_a9_qemu --enable-tests --enable-posix --disable-networking --enable-cxx
~~~~
### Build using 2 cores and install
~~~~
$ make -j 2
$ make install
~~~~
---

