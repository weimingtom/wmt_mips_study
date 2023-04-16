# wmt_mips_study
My MIPS study

## FPGA  
* https://github.com/weimingtom/wmt_mips_study/blob/master/fpga_001.md  

## TODO
* (IMP) Compile mingw mips cross gcc version 2    
* (IMP) https://github.com/ljkgpxs/virtualnoah  
* (IMP) https://github.com/OpenNoah/virtualnoah  
* (IMP) gxemul for godson 1 and 2 and mips  
* (IMP) skyeye and skyeye testcases for godson and mips    
* naken_asm  
* gcc -S for qtspim ((IMP) can see Simulizer-0.43-beta/gcc-mips.sh how to process gcc output)    
* see https://github.com/weimingtom/wmt_ai_study/blob/master/fpga_cpld_001.md  
* openwrt & buildroot   
* golang or rust baremetal / bare, simulator (emulator), compiler, etc  
* (IMP) ucosii  
* (IMP) Simulizer-0.43-beta  
* u-boot qemu  
* freertos, https://github.com/lengdongwl/Ls1bTest  
https://github.com/mugenZebra/UNO32-freeRTOS-port  
* u-boot for ls232, 
https://github.com/deepke/u-boot-mips  
https://github.com/gnaygnil/ls1c_robot_uboot  
* uno32  
https://github.com/rkujawa/chipKIT-minimal-application  
https://github.com/chipKIT32/PIC32-avrdude-bootloader  
* https://github.com/NJU-ProjectN/nemu  
(risc-v) https://github.com/OpenXiangShan/NEMU  
see https://www.bilibili.com/video/BV1Zb4y1k7RJ/  
* https://github.com/cyyself/cemu  
* (see cemu) https://github.com/z4yx/ucore-thumips/tree/for-ls232-soc_up  
* (TODO) https://github.com/grantae/mips32r1_xum/tree/master/Software/demos/XD1_Hello/src/os  
* https://github.com/evosynth/led_flash_wi-fire  
* 数字设计和计算机体系结构, MIPSfpga  
* DDCA2e_HDL_03-11-2015.zip  
07-mipssingle.sv, From Section 7.6 of Digital Design & Computer Architecture    
07-mipsmulti.sv  
* DDCA_Labs_companion.zip  
Lab 9: MIPS Single-Cycle Processor  
Lab 10: Multicycle Processor (Part 1)  
Lab 11: Multicycle Processor (Part 2)  
* MIPS Embedded OS (MEOS)  

## TODO, gcc -S, asm volatile, for QtSpim    
* (TODO) (IMP) use gcc-2.95.3 cross mips to gcc hello.c -S -mno-explicit-relocs, need comment jal __ main, why ???
```
jal	__main
```
* https://blog.csdn.net/yt_42370304/article/details/84982864  
* use "r" instead of "m" ???  
```
    asm volatile(
        "add $a0, $zero, %0;"
        "addi $v0, $zero, 4;"
        "syscall;"
	:
	:"m" ("The sum from 0 .. 100 is "));
```  
* use la ???, instead %lo() and %hi(), see -mno-explicit-relocs (high version gcc not support ???)    
```
	la $3, $LC0
	add $a0, $zero, $3
	addi $v0, $zero, 4
	syscall;
```
* E:\android-ndk-r10e\toolchains\mips64el-linux-android-4.9\prebuilt\windows\bin\mips64el-linux-android-gcc -march=r3000 -g0 -s hello.c -S  
* https://blog.csdn.net/weixin_40751723/article/details/120295374
* https://github.com/shihyu/Qemu.git
* https://github.com/EduRenesto/indy/blob/ae9485e8b8731a223b3c153280d798808836b7d5/res/extra/90.simple.c
* https://github.com/asherShores5/CompilerButBad/blob/d6a73cdd1c97bb9436cfd1bf78357f1510f9b689/MIPScode.h
* https://github.com/search?l=C&q=syscall+4+print_str+mips&type=Code  
* 安装mips编译器和模拟器/mips GCC编译环境搭建  
* mips-sde-elf-gcc  example.c -S -mno-explicit-relocs  
* https://blog.csdn.net/wfxzf/article/details/88974144  

## barebone hello, for qemu -machine mipssim    
* Jun Sun's Linux MIPS Porting Guide  
* http://web.archive.org/web/20160322170852/http://linux.junsun.net/porting-howto/  
* barebone_v1_success_mipssim_ubuntu140432_sde.tar.gz  
```
#LOADADDR = 0xa0040000
LOADADDR  = 0x81000000
RAMSIZE = 0x00100000		# 1MB
# or 0x1000 # 4k

CC =       $(CROSS_COMPILE)gcc -EL -fno-builtin
LD =       $(CROSS_COMPILE)ld -EL
```
```
//#define         BASE                    0xb0000080
#define         BASE                    0xbfd003f8
//mips:    0xb4000000;
//mipssim: 0xbfd00000;
//#define UART0_ISA_OFF   0x3f8
```
* https://gitee.com/caogos/qemu_gdb_mips_hello  
* qemu_gdb_mips_hello-master_v1_ubuntu140432_sde.tar.gz  
* https://github.com/petersho/qemu-mips-hello  

## doc  
* https://github.com/grantae/mips32r1_xum/tree/master/Documentation/MIPS  
* https://pages.cs.wisc.edu/~larus/HP_AppA.pdf  

## mips linux (vmlinux), for qemu -machine mipssim (and for -machine mips)      
* https://cdn.kernel.org/pub/linux/kernel/v3.x/linux-3.5.7.tar.gz  
* https://www.linux-mips.org/wiki/Porting  
* https://www.linux-mips.org/wiki/Kernel_Build  
* https://www.linux-mips.org/wiki/MIPSsim  
* https://www.linux-mips.org/wiki/Emulators  
* linux-2.x maybe ok  
* https://github.com/kholia/mips-hacking  

## loongson linux (vmlinux), ls1b defconfig, linux-2.6.3, 4.19, 5.3, for qemu (need src mod) -machine ls1b    
* https://cdn.kernel.org/pub/linux/kernel/v5.x/linux-5.2.tar.gz  
* https://gitee.com/loongsonlab/qemu  
* https://gitee.com/loongsonlab/loongson  
* see loongsonlab/loongson, for some prebuilt firmware, for example, initrd and vmlinux / vmlinuxz (without pmon)  
* https://github.com/tinyclub/qemu-mipsel-ls232  
* https://gitee.com/loongsonlab/linux-2.6.32  
* loongson_mod_v2_self_build_linux.tar.gz, not through pmon    
* NOTE: need to add 115200 to vmlinux boot command line:  
```
root=/dev/ram console=ttyS0,115200 rdinit=/linuxrc 
```
* how to build busybox and linux 5.2    
```
xubuntu200464  
sudo apt install gcc-mipsel-linux-gnu
```
```
xubuntu200464  

$ cd busybox-1.20.2
$ make ARCH=mips CROSS_COMPILE=mipsel-linux-gnu- defconfig
$ make ARCH=mips CROSS_COMPILE=mipsel-linux-gnu- menuconfig
Build Options--->Build BusyBox as a static binary(no shared libs)
Login/Password Management Utilities--->passwd(uncheck)
Miscellaneous Utilities--->time(uncheck)
Networking Utilities--->inetd(uncheck)ntpd(uncheck)
Runit Utilities--->all(uncheck)
* Then, (modify shell/shell_common.c) put '#if 0.. #endif' to shell/shell_common.c's 
printlim() inside, comment inside code
* Then, (modify shell/shell_common.c) put '#if 0.. #endif' to shell/shell_common.c's 
shell_builtin_unlimit(char **argv) inside, comment inside code

* see https://github.com/fdu/STM32F429I-disco_Buildroot/issues/1
Init Utilities--->init->Support reading an inittab file(uncheck)
* Then (modify nit/init.c, put /*...*/ inside) comment strings (tty2...4) in file nit/init.c, like this:
/*new_init_action(ASKFIRST, bb_default_login_shell, VC_2);
new_init_action(ASKFIRST, bb_default_login_shell, VC_3);
new_init_action(ASKFIRST, bb_default_login_shell, VC_4);*/

$ make ARCH=mips CROSS_COMPILE=mipsel-linux-gnu-
$ make ARCH=mips CROSS_COMPILE=mipsel-linux-gnu- install
```
```
（for busybox）

$ cd _install
$ mkdir -p proc sys dev etc etc/init.d
$ gedit ./etc/init.d/rcS
#!/bin/sh
mount -t proc none /proc
mount -t sysfs none /sys
/sbin/mdev -s
ifconfig lo up
ifconfig eth0 10.0.2.15 netmask 255.255.255.0
route add default gw 10.0.2.1
$ chmod +x ./etc/init.d/rcS
$ cp etc/init.d/rcS rcS
$ cd /dev
$ sudo mknod -m 660 console c 5 1
$ sudo mknod -m 660 null c 1 3
```
```
（for linux）

$ make ARCH=mips CROSS_COMPILE=mipsel-linux-gnu- loongson1b_defconfig
$ make ARCH=mips CROSS_COMPILE=mipsel-linux-gnu- menuconfig
General setup--> Initial RAM filesystem and RAM disk (check)
	Initramfs source file(s): /home/wmt/work_loongson/_install/
kernel hacking--->Built-in kernel command line
	(x) default string: root=/dev/ram console=ttyS0 rdinit=/linuxrc init=/linuxrc
	default string: root=/dev/ram console=ttyS0,115200 rdinit=/linuxrc
$ make ARCH=mips CROSS_COMPILE=mipsel-linux-gnu-
```
* 嵌入式Linux系统设计及应用-基于国产龙芯SOC3.1.0  
* https://mirrors.ustc.edu.cn/loongson/loongson1b/  
* https://mirrors.ustc.edu.cn/loongson/loongson1c_bsp/  
* https://github.com/z4yx/ucore-thumips/tree/for-ls232-soc_up  
* Buildroot 龙芯1C支持指南  
https://www.cnblogs.com/zzb-Dream-90Time/p/7111612.html  
* https://github.com/sundm75/Loongson-Smartloong-V3.0-RTT  
* https://files.loonglab.cn:8000  
* http://www.openloongson.org/
* https://www.bjlx.org.cn  
* https://github.com/KianWeng/loongson-ejtag  
* https://gitee.com/loongarch_community/Loongson-1c300b-OpenHarmony  
* https://github.com/loongson-gz/qemu  
* https://github.com/loongson-gz/ls1b-linux-3.18  
* https://github.com/loongson-gz/loongson_1b_ejtag  
* https://github.com/loongson-gz/loongson_1b_toolchain  
* https://github.com/loongson-gz/loongson_1b_linux_2.6.21.5  
* https://github.com/Red54/loongson1-linux-3.5  
* https://github.com/sundm75/Loongson-Smartloong-V2.0  
* 用“芯”探核: https://github.com/chenhuacai/linux-ulek  

## pmon (a bootloader for loongson) for loongson (here not boot vmlinux), for qemu (need src mod）-machine ls1b      
* https://mirrors.ustc.edu.cn/loongson/  
* https://gitee.com/brep/loongson1-pmon  
* https://gitee.com/loongsonlab/qemu  
* work_pmon.tar.gz  
* https://blog.csdn.net/u012101272/article/details/123578005  
* www.douban.com/note/184920595/  
* https://gitee.com/CaesarKarry/embedded_godson_1c300b  
* https://sites.google.com/site/kontais/gxemul, gxemul-0.4.3.godson.tar.gz, only for loongson2 64bit, not good    
* https://github.com/lshw/loongson1-pmon  
* https://github.com/loongson-gz/loongson_1b_pmon  
* https://github.com/loongson-gz/pmon-ls1x  
* build method:  
qemu: https://gitee.com/loongsonlab/qemu  
pmon: loongson1-pmon (from https://gitee.com/brep/loongson1-pmon ?)  
```
xubuntu 200464
prepare, see https://github.com/sergev/qemu/wiki
$ sudo apt-get install libpixman-1-dev libfdt-dev zlib1g-dev libglib2.0-dev libsdl-dev
see 	(IMP) qemu loongson build mothod!!!!
see 	(IMP) pmon loongson build mothod!!!!
```
```
(build qemu source mod for ls1b)  
$ git clone https://gitee.com/loongsonlab/qemu
$ cd qemu
$ mkdir build2
$ cd build2
$ ../configure --target-list=mipsel-softmmu --disable-werror --prefix=/home/wmt/work_pmon/qemu_pmon2
$ make
$ make install
```
```
(build pmon for ls1b)  
$ cd ../../loongson1-pmon  
$ ./build_ls1b_dev.sh  
(get pmon_ls1b_dev.bin)  
```
* run method:  
```
$ cd qemu_pmon2/bin
$ SERIAL=2 ./qemu-system-mipsel -M ls1b -serial stdio -bios pmon_ls1b_dev.bin 
```
* https://github.com/weimingtom/loongson1-pmon_fork  
* https://github.com/weimingtom/qemu_pmon_fork  
* (not good) 龙芯杯无开发板如何开发和调试linux  
https://blog.mxdon.cool/2021/无开发板如何开发linux系统内核/  

## xv6-mips, for qemu -machine mips (and -machine mipssim is ok, need modification)    
* https://github.com/varmil/xv6-mips  
* (not good) https://github.com/nullpo-head/xv6-mips  
* xv6-mips-new_from_varmil_success_no_some_seconds_crash.tar.gz  
* https://github.com/SKT-CPUOS/xv6-loongarch-exp  

## ucore, ucore-thumips (and for qemu -machine mipssim?)      
* https://github.com/Lan1keA/BIT-ucore_mips  
ucore_v3_success_from_Lan1keA_BIT-ucore_mips-master.tar.gz  
qemu-system-mipsel -M mipssim -m 32M -kernel ucore-kernel-initrd_2  
* https://github.com/chyyuu/ucore_os_plus/tree/clang-dev  
* https://github.com/chyh1990/ucore-thumips  
* https://github.com/chyh1990/qemu-thumips  
* https://github.com/Lan1keA/ucore-mips-with-comment  
* 基于龙芯FPGA开发板的计算机系统综合实验  
https://github.com/oscourse-tsinghua/LoongsonCsprj2017-manual  
https://oscourse-tsinghua.gitbook.io/loongsoncsprj2020-manual/ucore  
* https://www.bookstack.cn/read/simple_os_book/README.md  
* uCore OS实验指导书和源码网址 (2020)  
https://github.com/chyyuu/ucore_os_docs  
* ucore实验指导书  
https://chyyuu.gitbooks.io/ucore_os_docs/content/  
ucore labs 1-8 源码和参考答案 
https://github.com/chyyuu/ucore_lab  
os tutorial lab  
https://github.com/chyyuu/os_tutorial_lab  
* https://github.com/z4yx/ucore-thumips/tree/for-ls232-soc_up  


## hos-mips, based on Tsinghua ucore OS, can run with gxemul 0.6.1 mod    
* https://github.com/MrShawCode/hos-mips/tree/gxemul   
* https://github.com/klx3300/gxemul-hos  
see https://github.com/MrShawCode/hos-mips/blob/gxemul/gxemul_run.sh  
gxemul -E oldtestmips -C R6000 -M 512 obj/kernel/ucore-kernel-initrd  
work_hos_v1.tar.gz  

## rt-thread 20201229, for qemu -machine mipssim  
* rt-thread_back_to_202012291854_min.zip  
* Neweast version may crash  
* https://gitee.com/rtthread/rt-thread  
* https://blog.csdn.net/u014689277/article/details/121490983  
* LOONGSON派二代 RTthread  

## Topsy, for mipseb, run on Java Simulator (MipsSimulator)    
* https://github.com/pahihu/Topsy  
* https://github.com/pahihu/MipsSimulator  
* Topsy-master_v5_xu_success2.tar.gz  
* Topsy-master_v5_xu_success2_MipsSimulator2.7z  
* http://web.archive.org/web/20041010204139/http://www.tik.ee.ethz.ch/~topsy/index.html  
* http://web.archive.org/web/20041012105224/http://www.tik.ee.ethz.ch/~gfa/MipsSim.html  
* https://www.rose-hulman.edu/Class/se/csse490/cs490-csa/project/os/  
* https://www.rose-hulman.edu/Class/se/csse490/cs490-csa/project/os/topsy.srec  
* https://github.com/pahihu/Topsy/blob/master/User/link.scr  
* need to mod User/link.scr, add 0x80040000 offset to every segment !!!
```
 .rodata . : AT( 0x80040000 + ADDR(.rodata) )
 .data . : AT( 0x80040000 + ADDR(.data) )
 .sbss . : AT( 0x80040000 + ADDR(.sbss) )
 .bss . : AT( 0x80040000 + ADDR(.bss) )
/* make 0x80040000 offset to every segment */
```
* (TODO) https://github.com/drh/lcc  

## BUAA-OS, run on gxemul    
* https://github.com/login256/BUAA-OS-2019/tree/lab6  
* Need to add -d fs.img to run.bash or gxemul command line  
* https://github.com/login256/BUAA-OS-2019/tree/master  
* https://github.com/fmars/MIPS_OS_Kernel  
* login256_BUAA-OS-2019-lab6_run_success.tar.gz  
* https://github.com/rfhits/Operating-System-BUAA-2021  
* https://github.com/Niupple/BUAA-OS-Niupple  
* https://github.com/refkxh/BUAA_OS_2020Spring  
* https://github.com/Coekjan/SOMOS  

## xinu, for qemu mipsel -machine mips (mipssim not work)  
* https://github.com/xinu-os/xinu  
* cd compile; make  
* https://xinu.cs.mu.edu  
* xinu-master_v4_xubuntu_mips_success.tar.gz  
* (TODO) http://www.mscs.mu.edu/~brylow/xinu/  
* (OLD) xinu_mips-latest.tgz, xinu_mips-latest.tar.bz2  
* (NEW) xinu-master.zip  
* wrt54gl, wrt160nl, (new) wl330ge, e2100l, arm rpi  
* 操作系统设计:Xinu方法  
* 《操作系统设计：xinu方法》实验环境的搭建  
* https://blog.csdn.net/cang_xing/article/details/79166001  
* https://www.cs.purdue.edu/homes/comer/  
* https://uclibc.org/downloads/binaries/0.9.30.1/cross-compiler-mips.tar.bz2  
* (dead) http://xinu.cs.purdue.edu/files/Xinu-code-MIPS.tar.gz  
* https://github.com/robert-w-gries/rxinu  
* https://xinu.cs.purdue.edu  
* https://www.cs.purdue.edu/homes/comer/downloads/Xinu_Book_And_Code/other/Older_Versions/Xinu-code-MIPS.tar.gz  
* https://github.com/robinkrens/xinu-for-stm32  
* https://github.com/jarrocha/XinuBBB   
* https://github.com/9MMMinor/avrXinu-V7  
* http://se.fi.uncoma.edu.ar/xinu-avr/  
* https://github.com/zrafa/xinu-avr  

## os161, running on C simulator (sys161, for mipseb)    
* http://www.os161.org  
* https://student.cs.uwaterloo.ca/~cs350/common/Install161NonCS.html  
* https://student.cs.uwaterloo.ca/~cs350/common/OS161main-S07.html  
* https://student.cs.uwaterloo.ca/~cs350/common/Install161.html  
* https://student.cs.uwaterloo.ca/~cs350/common/WorkingWith161.html  
* work_os162_v1_success_some.tar.gz  

## (TODO) loongson / godson fpga  
* https://github.com/huitailangyz/B0911009Y-Computer-Architecture-Lab  
* https://github.com/poorjobless/cpu_gs232  

## (TODO) naken_asm  
* https://www.mikekohn.net/micro/naken_asm.php  
* https://github.com/mikeakohn/naken_asm  

## (TODO) qtspim  
* https://pages.cs.wisc.edu/~larus/HP_AppA.pdf  
* https://sourceforge.net/p/spimsimulator/code/HEAD/tree/  
* https://pages.cs.wisc.edu/~larus/spim.html  
* https://ecs-network.serv.pacific.edu/past-courses/2012-fall-ecpe-170/tutorials/qtspim-tutorial  
* QtSpim的数据段代码段可能是某种古老r3000机器的布局，但似乎也兼容mips32。我以前以为设置中的异常处理器是  
打开一个程序，其实是用来替换内置的boot汇编文件，或者不使用boot代码：  
* 可以加载多个.s汇编文件，会连接加载到同一个text段内，接在上一个的末尾。但不能批量添加，   
需要手工逐个加。所以加载汇编文件的菜单操作其实相当于接在内置异常处理器的.text段代码后面。  
* 汇编文件中.text的起始地址（例如.text 0x400000）参数只允许一定规则的偏移，例如只能40_0080  
* 汇编文件中.text和.ktext必须在text段和ktext段范围内，例如40_0000至44_0000之间。这个范围似乎是固定的  
* 设置中的异常处理器就是ktext段bootloader的代码（详细见spimsimulator源代码仓库中的exceptions.s，  
可以在sf的仓库中看到qtspim的源码）  
* 如果去掉异常处理器前面的勾，然后重启qtspim，或者菜单Reinitial Simulator，8000_0000的代码会清空。   
也可以自己参照exceptions.s的代码替换自己的boot汇编  
* 实际上设置中关闭内置的异常处理器汇编（去除勾），也可以正常运行汇编。可以通过菜单中Run Parameter   
修改运行的起始地址，默认是40_0000。对运行的影响比较少，仍然可以syscall，只是运行到最后可能会报错，或者用单步运行  
* 有时候菜单Reinitial Simulator也会出问题，导致加载汇编文件失败。最好是重启exe  
* 我觉得设置中的bare machine按钮没什么用，似乎无法修改段的起始地址的规定范围，几乎总是用simple machine就可以了  

## litebsd, retrobsd    
* https://github.com/sergev/LiteBSD  
* https://github.com/sergev/qemu/wiki/RetroBSD-Example  
* https://github.com/RetroBSD/retrobsd  
* https://github.com/zyy0721/Minisys-OS/blob/master/boot/boot.S  
* https://github.com/sergev/LiteBSD/releases/tag/tools  
* gcc-4.8.1-mips-linux.tgz  

## (TODO) virtualmips  
* https://code.google.com/archive/p/virtualmips  
* https://github.com/RetroBSD/retrobsd/tree/master/tools/virtualmips  
* virtualmips-0.01_run_success_need_libelf-dev.tar.gz  

## v6pic32  
* https://codeberg.org/zerocool32/v6pic32  

## nachos  
* https://homes.cs.washington.edu/~tom/nachos/  

## uclinux on psp 0.22  
* psplinux, tested on real machine (for example PSP2000), but ppsspp and jpcsp not work  
* uclinux_on_psp-0.22.zip  
* https://sites.google.com/site/jacksonm88/  
* https://sites.google.com/site/linuxonpspproject/  
* https://sites.google.com/site/wwwjalinux/linuxonpsp.htm  

## qemu-mt7628  
* https://github.com/newluhux/qemu-mt7628  

## (TODO) openwrt mips, for qemu -machine malta  
* https://github.com/cclinuxer/openwrt/blob/master/target/linux/malta/README  
* https://cclinuxer.gitee.io/2021/01/OpenWrt进行qemu模拟/  
* https://github.com/openwrt/openwrt/blob/master/target/linux/malta/README  

## (TODO) buildroot mips, for qemu -machine malta  
* https://github.com/buildroot/buildroot/blob/master/board/qemu/mips32r2el-malta/readme.txt  
* https://github.com/buildroot/buildroot/blob/master/configs/qemu_mips32r2el_malta_defconfig  

## rcore, Rust version of THU uCore OS Plus  
* https://github.com/rcore-os/rCore  

## virtualnoah, NP1100, JZ4740, qemu-NP_120730    
* https://github.com/ljkgpxs/virtualnoah  
* https://github.com/OpenNoah/virtualnoah  
* https://github.com/OpenNoahEdu/virtualnoah  

## skyeye, for mips au1100 and gs32eb1  
* skyeye-1.3.5_rc1.tar.bz2  
* skyeye-testsuite-1.3.4_rc1.tar.gz  
* skyeye-testsuite-1.3.4_rc1\skyeye-testsuite\dyncom\hello-mips  
* skyeye-testsuite-1.3.4_rc1\skyeye-testsuite\dyncom\hello_gs32eb1   

## PIC32 Architecture and Programming  
* https://johnloomis.org/microchip/pic32/resources.html  

## chipkit uno32    
* https://github.com/chipKIT32/PIC32-avrdude-bootloader  
* https://github.com/chipKIT32/chipKIT-digiboot  
* https://github.com/Microchip-MPLAB-Harmony/core_apps_pic32mx  

## pinguino32, PIC32  
* https://code.google.com/archive/p/pinguino32/downloads  

## crosstool-ng  
* https://code.lardcave.net/2015/02/10/1/  
```
$ ct-ng mips-unknown-elf
$ ct-ng menuconfig 
$ ct-ng build
```

## (TODO) mips32r1_xum, verilog and bare program  
* https://github.com/grantae/mips32r1_xum  

## (TODO) armadillo  
* https://github.com/ulfsigvardsson/armadillo  

## CS3650_MIPS32ALU  
* https://github.com/greyqwilson/MIPS32Processor_PreOwned  
* https://electrobinary.blogspot.com/2021/02/alu-design-in-verilog-using-mips.html  
* https://github.com/greyqwilson/CS3650_MIPS32ALU  

## NaiveMIPS  
* https://github.com/z4yx/NaiveMIPS-HDL  
* https://github.com/z4yx/ucore-thumips  
* https://github.com/z4yx/qemu-naivemips  

## step_into_mips  
* https://github.com/lvyufeng/step_into_mips  
* https://www.bilibili.com/video/BV1pK4y1C7es/  
* 教你写一个简单的CPU  
* 这个是单周期mips（出自重庆大学），没有实现多周期mips，  
* 作者说这个是比较靠谱（好）（龙芯）的开源教学实现  

## minimips32  
* https://github.com/study34668/MiniMIPS32  

## picomips  
* https://github.com/karthik-0398/picoMIPS  

## edu.cornell.cs3410, mips logisim, cs3410.jar  
* https://gitee.com/ForthewinQ/MIPS-CPU  

## mipsfpga-plus, schoolMips, xilfpga    
* (TODO) https://github.com/flsgavin/MIPSfpga-Boot    
* https://github.com/zyy0721/Minisys-OS  
* https://github.com/MIPSfpga/schoolMIPS/tree/05_pipeline_ahb/program/00_counter  
* https://github.com/MIPSfpga/mipsfpga-plus/blob/master/programs/12_linux/patches/MIPSfpga_linux.patch  
* https://github.com/zhelnio/ubuntu-hdl-tools-install  
* MIPSfpga_GSG_v2.0.0.zip  
* mipsfpga sword  
* mips模型机在Sword板子部署在FPGA  
* https://www.jianshu.com/p/86e0889755ca  
* https://github.com/FlyGinger/MIPSfpga-on-SWORD  
* https://github.com/flsgavin/MIPSfpga-Boot  
* http://www.sword.org.cn/courses/digital_logic  
* https://gitee.com/SWORDfpga/ComputerArchitecture/tree/master  
* https://github.com/MIPSfpga/schoolMIPS  
* 数字设计和计算机体系结构 原书第2版, P.433  
* https://github.com/u-boot/u-boot/tree/master/board/imgtec/xilfpga  
* linux-4.4 to 4.14  
* https://github.com/torvalds/linux/tree/v4.4/arch/mips/xilfpga   
* https://github.com/torvalds/linux/tree/v4.14/arch/mips/xilfpga  

## mips, nscscc  
* https://github.com/nscscc2019ucas/nscscc2019ucas/blob/master/display/soc_up/simu/soft/func/test.lds  
* https://github.com/lxfei7310/nontrivial-mips/tree/master/loongson/soc_run_os/simu/soft/func  
* https://github.com/leliyliu/augmips/blob/master/nscscc2019_release_v0.01/soc_run_os_v0.01/soc_up/simu/soft/func/start.S  
* https://github.com/imhcyx/nscscc-pmon  
* https://github.com/easter-mips/nscscc2020  
* 针对参加龙芯杯的若干建议, 可参考书籍  
* https://github.com/Silverster98/bit_nscscc_suggestion  
* pmon
* https://github.com/LoongSonOSTeamNKU/LoongsonCsprjManual/blob/master/chapter2.md  
* https://github.com/sime-chill/Build_A_CPU_In_1_Month  
* https://github.com/Gon-laze/GadgetMIPS-CPU-report  
* https://github.com/leliyliu/augmips  
* https://github.com/trialley/loongson_MIPS_demo  

## (TODO) freertos  
* https://github.com/MIPS/FreeRTOS/tree/mips  
* freertos_v5_success.tar.gz  
* (TODO) https://github.com/lengdongwl/Ls1bTest  
* https://github.com/grihey/FreeRTOS_mips  
* (TODO) (from ls1b) freertos_v2_failed.tar.gz  

## imgtec CI20, JZ4780，Creator Ci20, linux, android, openwrt  
* https://www.elinux.org/CI20_Hardware#Dedicated_UART_header  
* https://www.elinux.org/MIPS_Creator_CI20  
* (TODO) https://github.com/nfd/ci20-hello-world  
* (TODO) https://github.com/avahidi/ci20-baremetal  
* https://code.lardcave.net/2015/02/10/1/  
* http://code.lardcave.net/2015/02/10/2/  
* https://github.com/lucvoo/ll-mips  
* 在linux和buildroot里面出现的CI20开发板（都需要较新版，linux 5），  
* 其实就是君正的JZ4780（我以前说的那个用于电子辞典的是JZ4740）。  
* 另外qemu-system-mipsel里面不支持ci20，但我看了别人的模拟做法，  
* 似乎-machine mips就是可以模拟ci20的  
* (TODO) qemu-system-mipsel -machine mips is ci20 ???, see avahidi/ci20-baremetal  
* (TODO) u-boot command loads, to load srec, see avahidi/ci20-baremetal    
* 我搞明白为什么很多OS项目都喜欢输出srec格式文件（S-Record），其实是个梗，  
* 大概只有用过u-boot的人会明白。因为u-boot专门有个命令叫loads，  
* 这里的s就是srec的意思，可以通过串口粘贴srec文件内容（其实是一堆数字字母文本），  
* 就可以把固件烧录进去（srec内带有地址信息）  
* https://elinux.org/CI20_Dev_Zone#Source_Code  
* https://github.com/MIPS/CI20_linux  
* https://github.com/MIPS/CI20_u-boot  
* (android) https://github.com/MIPS/manifests  
* https://elinux.org/CI20_Distros  
* https://github.com/Pteridium/OpenWRT-experimental/tree/ci20-alpha  
* https://github.com/Pteridium/OpenWRT-CI20  
* https://github.com/avahidi/ci20-baremetal  
* https://github.com/wyatt8740/CI20_Linux  
* https://github.com/u-boot/u-boot/tree/master/board/imgtec/ci20  
* https://github.com/MIPS/CI20_u-boot/tree/ci20-v2013.10/board/imgtec/ci20  

## Creator Ci40, openwrt  
* https://github.com/CreatorDev/Ci40-platform-feed  
* https://github.com/CreatorDev/Ci40_helloworld  
* https://github.com/CreatorDev/ci-old  

## malta  
* https://github.com/u-boot/u-boot/tree/master/board/imgtec/malta  

## (TODO) cemu, seem can load vmlinux (no mips kernel config doc ???) and ucore    
* https://github.com/cyyself/cemu  
* https://github.com/cyyself/cemu/blob/master/docs/riscv64-linux.md  

## (TODO) NJU-ProjectN, nemu for mips, etc (only tested in x86)    
* https://github.com/NJU-ProjectN  
* https://github.com/NJU-ProjectN/nemu  
* https://github.com/s0duku/ics2020-s0duku  
* libc: https://github.com/s0duku/ics2020-s0duku/tree/main/abstract-machine/klib/src  
* linker script: https://github.com/s0duku/ics2020-s0duku/blob/main/abstract-machine/am/src/nemu/isa/mips32/boot/loader.ld  
* bootloader: https://github.com/s0duku/ics2020-s0duku/blob/main/abstract-machine/am/src/nemu/isa/mips32/boot/start.S  
* bare metal app: https://github.com/NJU-ProjectN/am-kernels/tree/master/kernels/litenes  
* os layer, but seem for bare metal: https://github.com/NJU-ProjectN/abstract-machine  
* ics2020-s0duku-main_v3.tar.gz, build method see apt_install.txt (only test in x86)    

## f32c  
* https://github.com/f32c/f32c  

## MangoMIPS32  
* https://github.com/RickyTino/MangoMIPS32  

## OpenMIPS, 自己动手写CPU    
* https://github.com/zach0zhang/Single_instruction_cycle_OpenMIPS  
* https://github.com/Tengs-Penkwe/OpenMIPS  
* https://github.com/yufeiran/OpenMIPS    

## build-a-cpu, logisim  
* https://github.com/ztreble/build-a-cpu  

## MiniMIPS32  
* https://github.com/study34668/MiniMIPS32  

## nontrivial-mips  
* https://github.com/lxfei7310/nontrivial-mips  

## MIPS246 Compiler & Assembler    
* https://github.com/ceie246/MIPS246_Software  

## cii, C Interfaces and Implementations, C语言接口与实现    
* https://github.com/drh/cii/blob/master/src/swtch.s  

## RIOT, before 2022.09  
* https://github.com/RIOT-OS/RIOT/tree/2022.07-branch/boards/pic32-wifire/include  
* https://gitee.com/bydvp/RIOT/tree/2022.07-branch/boards/pic32-wifire/include  

## zephyr, qemu machine malta  
* https://docs.zephyrproject.org/latest/boards/mips/qemu_malta/doc/index.html  

## nuttx, for pic32m  
* https://nuttx.apache.org/docs/latest/introduction/detailed_support.html#microchip-pic32mx2xx  

## (TODO) ucosii    
* mips_ucos_1.10.rar  
* ucos2.8-run-mips.rar  
* https://github.com/Tengs-Penkwe/OpenMIPS/tree/master/ucosii_sourcecode  
* https://github.com/yufeiran/OpenMIPS/tree/master/OpenMIPS/ucosii_sourcecode  

## Simulizer, for r3000  
* https://github.com/Simulizer/Simulizer  
* Simulizer-0.43-beta.zip, need jdk8  

## RTEMS  
* https://github.com/RTEMS/rtems/tree/master/bsps/mips  
* https://ftp.rtems.org/pub/rtems/releases/5/  
* https://blog.csdn.net/coolbacon/article/details/6089478  

## tcc, tinycc, tinycc-mips  
* https://github.com/lhzhang/tinycc-mips  
* 我发现有人吐槽tinycc（通常叫tcc）不支持MIPS，太难了（可不可以照着RISC-V来改），不过另一个编译器clang应该是可以输出MIPS的机器码  

## gcc  
* https://github.com/ChrisRx/mipsel-ecoff-toolchain  
* https://blog.csdn.net/ailuo58882/article/details/102270410  
mips-elf-gcc交叉编译环境的建立 (转载)  
* (gcc-4.4.6, not found) https://www.mips.com/linux-toolchain/  
* (see mips_linux_toolchain_src-1.1.tar.bz2) https://ir.nctu.edu.tw/bitstream/11536/44056/1/950301.pdf  
* (gcc-4.2.1) uclinux: https://github.com/Krush206/uclinux-mipsel-toolchain  
* (gcc-4.1.2) uclibc : https://www.uclibc.org/downloads/binaries/0.9.30.1/cross-compiler-mipsel.tar.bz2  
* (gcc-4.2.1) Aboriginal Linux : http://landley.net/aboriginal/downloads/binaries/cross-compiler-mipsel.tar.gz  
* (gcc-4.8.2) https://www.linux-mips.org/wiki/Toolchains  
* (gcc-6.3.0) https://stackoverflow.com/questions/42022659/how-to-get-a-smaller-toolchain-from-scratch  
* (gcc-4.3.2) rtems : https://ftp.rtems.org/pub/rtems/archive/windows/4.9/build-5/rtems4.9-tools-mips-5.exe  
* rtems gcc cygwin version (not found) see https://blog.csdn.net/coolbacon/article/details/6089478  
* (gcc-4.2-85 and above, Sourcery G++ Lite 4.2-85) https://sourcery.sw.siemens.com/GNUToolchain/subscription3130?lite=MIPS  
* https://gitee.com/bytes33/MIPS-TOOLS    
* https://gitee.com/bei_yi_ning/mips_tools_win  
* (gcc-3.0.4) vmips, unmodified versions of gcc-3.0.4, and binutils-2.15, configured for mipsel-ecoff, and compiled for cygwin :  
http://www.dgate.org/vmips/utils/mips-tools/cygwin/cygwin-mips-tools.tar.gz  
http://www.dgate.org/vmips/utils/mips-tools/cygwin/  
need cygwin1.dll, can copy from WinAVR-20100110, from WinAVR-20100110-install.exe  
https://sourceforge.net/projects/winavr/files/WinAVR/20100110/  
```
>mipsel-ecoff-gcc -v
Reading specs from ../lib/gcc-lib/mipsel-ecoff/3.0.4/specs
Configured with: ../gcc-3.0.4/configure --prefix=/usr/local/mipsel-ecoff --target=mipsel-ecoff 
--disable-shared --disable-nls --with-gnu-as --with-gnu-ld
Thread model: single
gcc version 3.0.4
```

## clang, llvm-gcc  
* https://github.com/llvm/llvm-project/blob/main/lld/test/ELF/mips-32.s  

## lcc  
* https://github.com/drh/lcc  

## qemu  
* https://www.aurel32.net/info/debian_mips_qemu.php  
* https://people.debian.org/~aurel32/qemu/mipsel/  
* https://repo.or.cz/qemu/qemu-loongson.git  
* https://repo.or.cz/qemu/qemu-JZ.git  

## mips_os  
* https://github.com/LinHeLurking/mips_os  

## 从一道mips题目学习搭建mips环境及ROP  
* https://cloud.tencent.com/developer/article/1745278  
* https://github.com/Q1IQ/ctf  

## X1000 RT-Thread-XBurst  
* https://github.com/XBurst/RT-Thread-XBurst/tree/master/bsp/x1000  
* https://github.com/Real-Thread/bsp_x1000  
* https://github.com/RT-Thread/rt-thread/tree/stable-v3.0.x/bsp/x1000  

## qemu, mipsel firmware emulation for auto-testing purposes  
* https://github.com/lunixoid/qemu_mips  

## u-boot, u-boot qemu    
* https://u-boot.readthedocs.io/en/v2020.04/board/emulation/qemu-mips.html#limitations-comments  
* https://u-boot.readthedocs.io/en/latest/board/emulation/qemu-mips.html  
* some mips boards not in documents, but in source  
* https://github.com/u-boot/u-boot/tree/master/board/imgtec  

## aoR3000, for r3000  
* https://github.com/alfikpl/aoR3000  

## vmips, for r3000  
* http://www.dgate.org/vmips/works.shtml  

## cui32  
* https://github.com/dwelch67/pic32_samples  
* https://code.google.com/archive/p/cui32/downloads  
* https://github.com/bcquitevis23/cui32  

## discobsd  
* https://github.com/chettrick/discobsd  

## picsimlab  
* https://lcgamboa.github.io/picsimlab_docs/0.8.10/Introduction.html#x2-10001  
* https://github.com/lcgamboa/picsimlab  

## UBIBoot  
* https://github.com/pcercuei/UBIBoot  

## xburst  
* https://github.com/Ingenic-community/Linux-XBurst  
* https://github.com/Ingenic-community/uboot-xburst  
* https://github.com/Ingenic-community/RT-Thread-XBurst  
* https://github.com/JaminCheung/x-loader  
* https://github.com/tobunto/ingenic-toolchain-v5.2  

## Cfern, mipsem, busybox-mips    
* https://github.com/alexyz/mipsem  
search baidupan, mipsem_v1.7z  
https://github.com/alexyz/mipsem/blob/master/src/cfern/Driver.java  
use -w  
* https://busybox.net/downloads/binaries/  
* https://busybox.net/downloads/binaries/1.16.1/busybox-mips  
not busybox-mipsel  

## 龙芯LoongIDE  
* mips-2015.05_from_sdelite_4.9.2_for_mips.rar  
* LoongIDE_from_loongide_1.2_beta3_setup.rar  
* loongide_1.2_beta3_setup.exe  

## (TODO) Educational kernel/rtos implementation for MIPS Malta QEMU  
* https://github.com/goniz/gzOS  

## arm_now  
* https://github.com/nongiach/arm_now  

## sysmips, in Java (need JDK8)      
* https://github.com/alexyz/sysmips  
* running MIPS 4kc malta linux rom (linux source build not tested, only rom file)   

## pcsx2  
* https://github.com/PCSX2/pcsx2  

## nu32  
* Embedded Computing and Mechatronics with the PIC32 Microcontroller  
* 嵌入式计算与机电一体化技术：基于PIC32微控制器  
* http://hades.mech.northwestern.edu/index.php/NU32  
* https://textbooks.elsevier.com/web/product_details.aspx?isbn=9780124201651&Search=nu32&SearchCriteria=Keyword  
* http://hades.mech.northwestern.edu/index.php/NU32_Software  
* PIC32Quickstart.zip  

## CuRT_v1_MIPS  
* https://github.com/algosenses/CuRT_v1_MIPS  
* https://github.com/Rafe/CuRT  
* https://github.com/jserv/CuRT  

## pic32, uno32  
* 经过我的努力，终于把变砖的uno32救回来了。之前没办法烧录bootloader的原因也找到了，  
是因为杜邦线的问题，导致无法检验设备id，我把杜邦线反转次序就正常了。  
烧录也不是很明白，我用的是IPE v6，但我不清楚怎么烧录成功的，  
可能是因为我勾选了高级模式，Allow Memory View，Program Memory，  
也可能不是这样做（待考），我先烧录一个别的hex再烧录bootloader，  
最后要拔出pickit3才能看到闪灯（？）  
* 只需要烧录bootloader，然后拔掉pickit3，就可以看到闪灯效果，不需要再烧录其他hex文件  
* 如果出现识别不到设备id，或者提示电压不够，  
请检查杜邦线是不是可能有一根不通（例如反转过来次序重新接或更换新的），  
或者重新插拔pickit3的usb  

## Fishino32, PIC32MX470F512HI/MR  
* http://www.fishino.it/arduinoide/package_fishino_index.json  
* https://fishino.it/fishino32.html  
* https://fishino.it/fishino-piranha-133.html  
PIC32MX470F512H-120I/PT  
* https://fishino.it/fishino-shark-135.html  
PIC32MX470F512L-120I/PF  

## (TODO) yamon, mips bootloader   
* https://github.com/binsgit/mips-yamon  
* https://www.mips.com/develop/tools/boot-loaders/  
* search baidupan, yamon-src-02.04.tar.gz  

## TinyMIPS  
* http://staff.ustc.edu.cn/~han/CS152CD/  

## (IMP) MIPS SDE-lite, sde-gcc, sde-run, sde-gdb, for Windows / Cygwin and Linux  
* http://staff.ustc.edu.cn/~han/CS152CD/Content/Software/SDElite/clickthru.html  
* http://staff.ustc.edu.cn/~han/CS152CD/, software->MIPS SDE-lite    
* (IMP) http://staff.ustc.edu.cn/~han/CS152CD/Content/Software/SDElite/sde-guide.pdf  
* Computer Organization and Design  
* (TOOD) MIPSSW-MSDE-v5.03.06.tgz\.\sde\examples\hello   
* (TODO) maybe sde-gdb can use mipssim ???  
* search baidupan, COD3E_计算机组成与设计.iso, 第3版  
* 计算机组成与设计：硬件/软件接口  

## mraa, libmraa  
* https://github.com/eclipse/mraa/blob/master/docs/linkit_7688.md  
* https://github.com/eclipse/mraa/blob/master/src/mips/mediatek.c  

## HUST OS ???  
* 华中科技大学计算机学院计算机组成原理课程设计, logisim run hex (?)        
* https://github.com/Starrylay/awesome-HUST-CS-MIPS-CPU  
* https://github.com/ver217/MIPS-CPU-TOY   
* mips-probe.jar  
* cs3410.jar  
* java -jar logisim-hust-20200118.exe  
* some risc-v  
* some mips java emulator code is in cs3410.jar  
* 有人做了logisim的mips器件插件，用于模拟mips，叫cs3410.jar，  
出处不详（可能是外面的课程，可能是闭源的），可以反编译，  
看到里面好像是有一个Java写的mips汇编器。。。  
有人甚至把它改成risc-v版和arm版。。。  
我没试过，有课程用到这个东西去模拟mips的cpu，  
有本叫《计算机组成原理实践教程——从逻辑门到CPU》  
* cs3410.jar: edu.cornell.cs3410.ProgramAssembler#main: 汇编器  
```
usage: ProgramAssembler <mips-asm-file>  
```
* mips-probe.jar: hust2020.Probe2#paintInstance: 反汇编器  
* Mars4_5.jar, MIPS汇编工具及测试用例4.7, 很多可以用mars运行的汇编例子  

## MIPS Embedded OS (MEOS)  
* https://github.com/MIPS/meos  

## 君正 X1500 ???    
* https://github.com/IceForgTW/X1500  

## mipseltools-gcc412-lnx26, 君正jz4740 gcc toolchain  
* https://gitee.com/piaoxuebingfeng/mipseltools-gcc412-lnx26  
