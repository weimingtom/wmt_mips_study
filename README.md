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
* see loongsonlab/loongson, 
* https://gitee.com/loongsonlab/linux-2.6.32  
* loongson_mod_v2_self_build_linux.tar.gz, not through pmon    

## pmon for loogson (here not boot vmlinux), for qemu (need src mod）-machine ls1b      
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

## BUAA-OS, run on gxemul    
* https://github.com/login256/BUAA-OS-2019/tree/lab6
* https://github.com/login256/BUAA-OS-2019/tree/master  
* https://github.com/fmars/MIPS_OS_Kernel  
* login256_BUAA-OS-2019-lab6_run_success.tar.gz  

## xinu, for qemu mipsel -machine mips (mipssim not work)  
* https://github.com/xinu-os/xinu  
* cd compile; make  
* https://xinu.cs.mu.edu  
* xinu-master_v4_xubuntu_mips_success.tar.gz  

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
* uclinux_on_psp-0.22.zip  
* https://sites.google.com/site/jacksonm88/  
* https://sites.google.com/site/linuxonpspproject/  
* https://sites.google.com/site/wwwjalinux/linuxonpsp.htm  

## qemu-mt7628  
* https://github.com/newluhux/qemu-mt7628  
