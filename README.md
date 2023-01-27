# wmt_mips_study
My MIPS study

## TODO
* (IMP) Compile mingw mips cross gcc version 2    
* (IMP) https://github.com/ljkgpxs/virtualnoah  
* (IMP) https://github.com/OpenNoah/virtualnoah  
* (IMP) gxemul for godson 1 and 2 and mips  
* (IMP) skyeye and skyeye testcases for godson and mips    
* naken_asm  
* gcc -S for qtspim  
* see https://github.com/weimingtom/wmt_ai_study/blob/master/fpga_cpld_001.md  
* openwrt & buildroot   
* golang or rust baremetal / bare, simulator (emulator), compiler, etc  

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

## mips linux (vmlinux), for qemu -machine mipssim (and for -machine mips)      
* https://cdn.kernel.org/pub/linux/kernel/v3.x/linux-3.5.7.tar.gz  
* https://www.linux-mips.org/wiki/Porting  
* https://www.linux-mips.org/wiki/Kernel_Build  
* https://www.linux-mips.org/wiki/MIPSsim  
* https://www.linux-mips.org/wiki/Emulators  
* linux-2.x maybe ok  

## loogson linux (vmlinux), ls1b defconfig, linux-2.6.3, 4.19, 5.3, for qemu (need src mod) -machine ls1b    
* https://cdn.kernel.org/pub/linux/kernel/v5.x/linux-5.2.tar.gz  
* https://gitee.com/loongsonlab/qemu  
* https://gitee.com/loongsonlab/loongson  
* see loongsonlab/loongson, for some prebuilt firmware, for example, initrd and vmlinux / vmlinuxz (without pmon)  
* https://gitee.com/loongsonlab/linux-2.6.32  
* loongson_mod_v2_self_build_linux.tar.gz, not through pmon    
* NOTE: need to add 115200 to vmlinux boot command line:  
```
root=/dev/ram console=ttyS0,115200 rdinit=/linuxrc 
```

## pmon (a bootloader for loogson) for loogson (here not boot vmlinux), for qemu (need src mod）-machine ls1b      
* https://mirrors.ustc.edu.cn/loongson/  
* https://gitee.com/brep/loongson1-pmon  
* https://gitee.com/loongsonlab/qemu  
* work_pmon.tar.gz  

## xv6-mips, for qemu -machine mips (and -machine mipssim is ok, need modification)    
* https://github.com/varmil/xv6-mips  
* (not good) https://github.com/nullpo-head/xv6-mips  
* xv6-mips-new_from_varmil_success_no_some_seconds_crash.tar.gz  

## ucore, ucore-thumips (and for qemu -machine mipssim?)      
* https://github.com/Lan1keA/BIT-ucore_mips  
* https://github.com/chyyuu/ucore_os_plus/tree/clang-dev  
* https://github.com/chyh1990/ucore-thumips  
* https://github.com/chyh1990/qemu-thumips  
* ucore_v3_success_from_Lan1keA_BIT-ucore_mips-master.tar.gz  

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

## BUAA-OS, run on gxemul    
* https://github.com/login256/BUAA-OS-2019/tree/lab6  
* Need to add -d fs.img to run.bash or gxemul command line  
* https://github.com/login256/BUAA-OS-2019/tree/master  
* https://github.com/fmars/MIPS_OS_Kernel  
* login256_BUAA-OS-2019-lab6_run_success.tar.gz  

## xinu, for qemu mipsel -machine mips (mipssim not work)  
* https://github.com/xinu-os/xinu  
* cd compile; make  
* https://xinu.cs.mu.edu  
* xinu-master_v4_xubuntu_mips_success.tar.gz  
* (TODO) http://www.mscs.mu.edu/~brylow/xinu/  
* (OLD) xinu_mips-latest.tgz, xinu_mips-latest.tar.bz2  
* (NEW) xinu-master.zip  
* wrt54gl, wrt160nl, (new) wl330ge, e2100l, arm rpi  

## os161, run on C simulator (sys161)    
* http://www.os161.org  
* https://student.cs.uwaterloo.ca/~cs350/common/Install161NonCS.html  
* https://student.cs.uwaterloo.ca/~cs350/common/OS161main-S07.html  
* https://student.cs.uwaterloo.ca/~cs350/common/Install161.html  
* https://student.cs.uwaterloo.ca/~cs350/common/WorkingWith161.html  
* work_os162_v1_success_some.tar.gz  

## (TODO) loogson / godson fpga  
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

## skyeye, for mips au1100 and gs32eb1  
* skyeye-1.3.5_rc1.tar.bz2  
* skyeye-testsuite-1.3.4_rc1.tar.gz  
* skyeye-testsuite-1.3.4_rc1\skyeye-testsuite\dyncom\hello-mips  
* skyeye-testsuite-1.3.4_rc1\skyeye-testsuite\dyncom\hello_gs32eb1   

## PIC32 Architecture and Programming  
* https://johnloomis.org/microchip/pic32/resources.html  

## chipkit uno32    

## imgtec CI20, JZ4780      
* https://www.elinux.org/CI20_Hardware#Dedicated_UART_header  
* https://www.elinux.org/MIPS_Creator_CI20  
* (TODO) https://github.com/nfd/ci20-hello-world  
* https://code.lardcave.net/2015/02/10/1/  
* http://code.lardcave.net/2015/02/10/2/  


## crosstool-ng  
* https://code.lardcave.net/2015/02/10/1/  
```
$ ct-ng mips-unknown-elf
$ ct-ng menuconfig 
$ ct-ng build
```

