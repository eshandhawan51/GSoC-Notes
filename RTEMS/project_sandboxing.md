# This document depicts the the arrangement of folders on my system.

---
~~~~
Home Folder (~): /home/eshan

~/development
	|
	|____/rtems
	|	|
	|	|____/5 	#- Directory for toolchain for rtems5
	|	|____/rsb 	#- contains RSB
	|	|____/kernel
	|		|____/erc32 			#- contains RTEMS kernel for SPARC
	|		|____/xilinx_zynq_a9_qemu 	#- contains RTEMS kernel for ARM
	|               |____/rv32imac                  #-contains RTEMS kernel for RISCV    
	|		|____/rtems			#- rtems clone from git repository
	|
	|
	|
	|
	|____/newlib
		|____/b-sparc-rtems5-newlib	#- newlib compiled for SPARC using rtems5 toolchain
		|____/b-arm-rtems5-newlib	#- newlib compiled fro ARM using rtems5 toolchain
		|____/newlib-cygwin		#- Clone of newlib from git repository


~~~~

---
