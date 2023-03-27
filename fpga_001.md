
## altera 64bit version 12  
* EP4CE10F17C8  
* 新起点FPGA开发板IO引脚分配表_v2_ref.xlsx  

## (TODO, IMP) MiniMIPS32  
* 计算机系统设计（上册）——基于FPGA的RISC处理器设计与实现  
* https://github.com/study34668/MiniMIPS32  
* minimips32_v8_20221114_坑未处理.rar  
* 计算机系统设计（下册）  

## cpu31_v4_e10_success.rar  

## 搭建你的数字积木——数字电路与逻辑设计（Verilog HDL&Vivado版）  
* https://github.com/xupsh/Digital-Design-Lab  
* http://www.tup.tsinghua.edu.cn/booksCenter/book_07172301.html  
* search baidupan, mipscpu_v2_e10_success.rar  

## minisys2_v3_e10_success.rar  

## minisys3_v1.rar  
## minisys_v1.rar  

## schoolMIPS, MIPSfpga  
* https://github.com/MIPSfpga/schoolMIPS  
* search MIPSfpga_GSG_v2.0.0.zip  
* (?) schoolMIPS_v2.rar  
* (?) mipsfpga_v1.rar    

## 重庆大学, 单周期(single cycle) mips  
* https://github.com/lvyufeng/step_into_mips  
* https://www.bilibili.com/video/BV1pK4y1C7es  

## 龙芯教育 / CPU设计实战, MIPS, LoongsonArch      
* 《CPU设计实战》实验资源  
* https://gitee.com/loongson-edu/cdp-lab  
* https://github.com/cebarobot/UCAS-CALab-mycpu_verify  
* https://github.com/cebarobot/UCAS-CALab-mycpu_axi_verify  
* https://github.com/cebarobot/UCAS-CALab-mycpu_sram_verify  

## ---


## MIPS, Digital Design and Computer Architecture  
* 数字设计和计算机体系结构 原书第2版  
* https://textbooks.elsevier.com/web/product_details.aspx?isbn=9780123944245  
* https://booksite.elsevier.com/9780123944245/?ISBN=9780123944245  
* DDCA_Labs_companion.zip, mipsmulti.sv (SystemVerilog)  
* DDCA2e_HDL_03-11-2015.zip, 07-mipssingle, 07-mipsmulti (VHDL and SystemVerilog, .vhd and .sv)    
* mipsfpga  
* https://github.com/MIPSfpga/digital-design-lab-manual  

## XUP官方指定的入门级FPGA教学板卡-Basys3  
* https://www.sytek.ltd/productinfo/1532427.html  

## 单周期mips, 搭建你的数字积木——数字电路与逻辑设计  
* https://github.com/xupsh/Digital-Design-Lab/tree/master/Chapter_14/RISC  

## mips的汇编方法（准确说是mips32el）：
（1）生成二进制的方法：用mars生成汇编二进制（参数参考schoolmips）；  
或者用gcc工具链Codescape生成，例如：  
mips-img-elf-as.exe -O0 -EL test.s  
mips-img-elf-objdump -S a.out  
mips-img-elf-objcopy -O binary -j .text a.out a.bin  
（2）示例代码：流水灯代码待考；参考mars的例子（只有一个）；  
参考schoolmips的例子（汇编或者用GCC生成的汇编）  

## mipsfpga sword  
* mips模型机在Sword板子部署在FPGA  
https://www.jianshu.com/p/86e0889755ca  
* https://github.com/FlyGinger/MIPSfpga-on-SWORD  
* http://www.sword.org.cn/courses/digital_logic  
* https://gitee.com/SWORDfpga/ComputerArchitecture/tree/master  

## f32c, risc-v or mips implementation    
* https://github.com/f32c/f32c  
* RISC-V助力SWORD生态系统演进   
* 近日，基于RISC-V指令集的软核CPU在SWORD4.0上顺利移植，给予用户对SWORD4.0的新体验，用户甚至可以通过Arduino IDE开发RISC-V应用。  
在SWORD4.0上移植的是基于RISC-V指令集的F32C开源CPU。CPU通过配置既可以支持RISC-V指令集也可以支持MIPS指令集。  
用户通过对Arduino IDE简单升级，可以使Arduino IDE支持SWORD4.0的RISC-V编译工作。图形化编程环境和大量Arduino范例都有利于用户进行应用开发。  
* https://www.sohu.com/a/272536883_652907  

## OpenMIPS, 自己动手写CPU  

## PicoMIPS  

## mips in cii (C Interfaces and Implementaions)  
* https://github.com/drh/cii/blob/master/src/swtch.s  
* search baidupan, cii20.zip  
* http://code.google.com/p/cii/downloads/detail?name=cii20.zip&can=2&q=
* https://github.com/drh/cii  
* search baidupan, C接口库  

## xv6-mips  
https://github.com/nullpo-head/xv6-mips  


## picomips  
https://github.com/karthik-0398/picoMIPS  
search csdn  

## ghidra, mips decompile  
* https://github.com/NationalSecurityAgency/ghidra/releases  

## cygwinmipselfgcc  
* https://sourceforge.net/projects/cygwinmipselfgcc/  


## (TODO) mips logisim, cs3410.jar      
* edu.cornell.cs3410  
* 计算机组成原理实践教程——从逻辑门到CPU  
* 控制器设计：MIPS单周期CPU_耳东哇的博客-CSDN博客_单周期mips  
* https://blog.csdn.net/weixin_43930851/article/details/106750718  
* https://gitee.com/ForthewinQ/MIPS-CPU  
* Logisim2.7.1下载并列出电路真值表、卡诺图。 - 腾讯云开发者社区-腾讯云  
* https://cloud.tencent.com/developer/article/2012197  
* 我看到有些课本mips书也吐槽MARS的内存布局，默认不是从0开始算。  
《计算机组成原理实践教程——从逻辑门到CPU》的解释是，因为MARS是带有MMU部件的虚存，  
而且不是哈佛体系。而通常用FPGA实现的MIPS软核是直接访问物理内存，  
而且是哈佛体系，所以这两个很难兼容，需要手工改MARS的虚存地址模式，让data段从0开始计算  

## MIPSsim  
* https://www.cnblogs.com/jiangxinnju/p/10090834.html  
* https://blog.csdn.net/capture3333/article/details/125665327  



## WinDLX  
* https://github.com/Justlovesmile/WindLX-Experiment  
* https://gitee.com/justlovesmile/WindLX-Experiment  
* https://cloud.tencent.com/developer/article/1918333  
* (exe files, only support windows xp) https://github.com/dlcPYY/WinDLX  
* 计算机系统结构  
* 计算机体系结构实验二——DLX/MIPS/RISC-V指令格式  
* https://blog.csdn.net/weixin_51529433/article/details/125910985   
* risc-v, venus  


## 计算机组成原理实践教程——从逻辑门到CPU  
* https://www.icourse163.org/course/HUST-1205809816#/info  
* 自己动手画CPU, by logisim    
* https://gitee.com/totalcontrol/hustzc/  


## loongnix, 龙芯   
http://www.loongnix.cn/zh/toolchain/GNU/  


## mips, 龙芯, 针对参加龙芯杯的若干建议, 可参考书籍    
* https://github.com/Silverster98/bit_nscscc_suggestion  
* pmon  
* https://github.com/LoongSonOSTeamNKU/LoongsonCsprjManual/blob/master/chapter2.md  

## NaiveMIPS  
* https://github.com/z4yx/NaiveMIPS-HDL  


## xilfpga linux, mipsfpga-plus linux  
从目前来看，似乎只有qemu是最简单的运行mips linux的方法。我查过，    
其实确实有一段时间xilfpga（就是常说的mipsfpga，不过这个开源项目早已经噶了）  
加入到linux源码树中，大概是在4.4到4.14之间，然后消失了（可能跑到别的地方或者被移除）。  
另外mipsfpga-plus也有关于加载linux内核的描述，当然开发板太贵不太适合搞来试验  

## mips 龙芯1c文档      
* http://codescape.mips.com/components/toolchain/2017.10-07/downloads.html  
* https://blog.csdn.net/caogos/article/details/78984158  
* https://gitee.com/caogos/OpenLoongsonLib1c  
* https://gitee.com/caogos/OpenLoongsonLib1c/tree/master/doc  


## cemu, mips and risc-v    
* https://github.com/cyyself/cemu  
* https://gitee.com/loongson-edu/la32r-Linux  

## mipssim  
* MipsSimulatorApplet.tar.gz  
* https://www.linux-mips.org/wiki/Emulators  
* http://web.archive.org/web/20041014015457/http://www.tik.ee.ethz.ch/~topsy/source.shtml  


## mips, Minisys-OS  
* https://github.com/zyy0721/Minisys-OS  

## MIPSfpga-Boot  
* https://github.com/flsgavin/MIPSfpga-Boot  

## u-boot mips  
* https://u-boot.readthedocs.io/en/v2020.07/board/emulation/qemu-mips.html  

## nuttx, rt-thread mips  

## gaia xv6, mips xv6, search memfs in Makefile, crosstool-ng       
* https://fuel.edby.coffee/posts/how-we-ported-xv6-os-to-a-home-built-cpu-with-a-home-built-c-compiler/  
* https://github.com/nyuichi/xv6  
* https://nullpo-head.github.io/emcc-gaia-simu/xv6.html  
* https://github.com/nullpo-head/xv6-mips  
* https://github.com/nullpo-head/emcc-gaia-simu  

## loongson  
* https://github.com/ForgotFun/loongson
* https://forgotfun.org/category/loongson/  
* https://github.com/lshw/loongson1-pmon  

## (IMP) Java mips simulator, can load vmlinux-3.2.0-4-4kc-malta  
* https://github.com/alexyz/sysmips

## https://gitee.com/loongsonlab/qemu  

## gxemul-0.4.3.godson.tar.gz  

## https://github.com/petersho/qemu-mips-hello  

## https://github.com/tinyclub/qemu-mipsel-ls232  

## https://github.com/zjutoe/abacusim  

## https://github.com/mikeakohn/naken_asm  

## https://github.com/jart/blink  

## FreeRTOS for MIPS  
* https://github.com/MIPS/FreeRTOS/tree/mips  
* https://www.mips.com/rtos-iot/  

## 龙芯baremetal  
* https://gitee.com/rtthread/rt-thread/tree/gitee_master/bsp/loongson/ls1cdev  
* http://www.loongide.com/content/  
* https://gitee.com/caogos/OpenLoongsonLib1c  

## mips, mipsfpga toolchain  
* https://github.com/zhelnio/ubuntu-hdl-tools-install  

## mips工具链  
* 找到sourcery的mips工具链，可以用于后续的研究。目前手头上有这4种mips工具链，  
* sourcery的sde（只支持elf），  
* codescape的mti（支持elf和linux），  
* ubuntu的gnu（似乎只支持linux），  
* 还有buildroot版的交叉工具链（支持elf和linux）。  
* 当然还有开发板的工具链可以用，例如从龙芯或者其他mipsel开发板的工具链那里拿来用  

## mips delay slot  
* 对比arm和mips，实际上mips有一些诟病的地方，mips似乎有一定的指令约束，叫delay slot，如果不正确的话会执行不下去。  
* 另外mips的版本可能会比arm多，导致工具链臃肿，例如最常见的R3000和4kC，我没搞明白怎么区分（可能类似arm9和cortex的关系）。  
* 但mips有个好处（也是坏处），它比arm要老，而且最常用于科研  
* https://blog.csdn.net/babyfans/article/details/6336476  

## mips  
* https://gitee.com/trialley/loongson_MIPS_demo  
* https://gitee.com/ingenic/mips-sde-elf  
* https://gitee.com/abignail/mips32-nemu  
* https://gitee.com/caogos/qemu_gdb_mips_hello  
* https://gitee.com/hao111xin/xv6-mips  
* https://github.com/nongiach/arm_now  
* gxemul can run vmlinux-2.6.32-5-4kc-malta_mipsel  
* MipsSimulator2_v1_Topsy-master_v1_success_use_codescape.tar  
* gxemul-0.4.3.godson.tar.gz  
* barebone.tar.gz  
* https://github.com/Lan1keA/ucore-mips-with-comment  
* https://github.com/sth1997/MIPS32S_CPU  
* https://github.com/z4yx/NaiveMIPS-HDL/blob/brd-NSCSCC/documentation/2016spring-OS.md  
* cemu  
* https://github.com/Gon-laze/GadgetMIPS-CPU-report  
* https://github.com/tinyclub/linux-lab  
* https://github.com/adofsauron/linux-kernel  
* https://gitee.com/loongsonlab/qemu  
* https://github.com/LinHeLurking/mips_os  
* https://github.com/ljkgpxs/virtualnoah  
* https://github.com/ljkgpxs/virtualnoah/blob/master/qemu-NP/hw/mips_jz.c  
* QEMU for JZ4740 ?????  
* https://github.com/OpenNoah/virtualnoah  
* https://github.com/newluhux/qemu-mt7628  
* Digital Design and Computer Architecture, 2nd Edition  
* https://textbooks.elsevier.com/web/product_details.aspx?isbn=9780123944245  
* 《数字设计和计算机体系结构第2版》有关于mipsfpga和mips的内容  
* minisys-os, for m14kc, mipsfpga,  
* https://github.com/zyy0721/Minisys-OS  
* https://github.com/mxzel/Minisys-OS  
* https://github.com/kholia/mips-hacking  
* https://github.com/loongson/qemu  
* https://github.com/RickyTino/MangoMIPS32  
* https://github.com/jpcsp/jpcsp   
* https://github.com/kontais/EFI-MIPS  
* https://github.com/jiegec/linux-gugumips  
* https://github.com/DaveeFTW/iplsdk  
* https://github.com/smalltree/shenglong/blob/master/x86emu/include/io.h  
* https://github.com/deepke/u-boot-mips  
* https://www.linux-mips.org/wiki/Emulators  
* https://github.com/hzshang/0ctf2020-flash  
* https://github.com/Ingenic-community/x-loader  
* https://github.com/michaekang/skyeye-testsuite/blob/master/dyncom/hello-mips/hello-mips.c  
* https://github.com/trivialmips/TrivialMIPS
* see https://github.com/rcore-os/rCore  
* (IMP) https://github.com/grantae/mips32r1_xum  
* https://github.com/NiklasKunkel/32-Bit-Multi-Cycle-Bare-MIPS-CPU  


## mips gcc, litebsd    
* https://github.com/sergev/LiteBSD  
* https://github.com/sergev/LiteBSD/releases/tag/tools  
* https://codeberg.org/zerocool32/v6pic32  
* (IMP) https://github.com/sergev/LiteBSD/wiki/ELF-toolchain  
* https://github.com/sergev/qemu/wiki  
* QEMU simulator for PIC32  
* https://www.microchip.com/forums/m842753.aspx  

## virtualmips, can load vmlinux, for adm5120, pavo (JZ4740)  
* https://code.google.com/archive/p/virtualmips/downloads?page=1  
* https://github.com/RetroBSD/retrobsd  

## naivemips  
* https://oscourse-tsinghua.gitbook.io/loongsoncsprj2020-manual/ucore/os_comp  
* https://github.com/z4yx/ucore-thumips  
* gcc-4.3-ls232.tar.gz  
* $ ./mipsel-softmmu/qemu-system-mipsel -machine soc_up -serial stdio -kernel ../ucore-thumips/flash.img  
* https://github.com/z4yx/u-boot-naivemips.git  
* mips-sde-elf-i686-pc-linux-gnu.tar.tar  
* https://github.com/xyongcn/LoongsonCsprj2017/blob/master/doc/soc_lite%E5%92%8Csoc_up%E4%BB%8B%E7%BB%8D_v0.01.pdf  
* https://gist.github.com/mentha/bbc6044e6cc39e38bc583b06b6bf9393  
* https://oscourse-tsinghua.gitbook.io/loongsoncsprj2020-manual/ucore/qemu  

## cutecpu  
* https://blog.csdn.net/Jelly_Zhou/article/details/126676735  
* search baidupan, cutecpu  
* https://space.bilibili.com/430527711/channel/seriesdetail?sid=526454  

## 龙芯 (in mips) pmon qemu  
* 龙芯杯无开发板如何开发和调试linux  
* https://blog.mxdon.cool/2021/无开发板如何开发linux系统内核/  
* https://gitee.com/loongsonlab/qemu  
* https://blog.csdn.net/weixin_45090728/article/details/124355432  
* see 参考文章  

## loongson, 龙芯  
* https://github.com/sundm75/Loongson-Smartloong-V2.0  
* https://github.com/sundm75/Loongson-Smartloong-V3.0-RTT  
* https://github.com/lshw/loongson1-pmon  
* https://github.com/lshw/loongson1-kernel3.18  
* https://github.com/lshw/pmon_unas  
* https://github.com/jcowgill/pmon-loongson  
* https://github.com/BarclayII/pmon-3amatx  
* (buildroot?) https://github.com/KianWeng/loongson-fsu  
* https://github.com/KianWeng/ls1b-pmon  
* https://github.com/imhcyx/nscscc-pmon  
* https://github.com/lshw/pmon_m5040  
* https://github.com/huitailangyz/B0911009Y-Computer-Architecture-Lab  
* https://github.com/loongson-gz/pmon-ls1x  
* https://github.com/Loongbian/loongson-simple-installer  
* https://github.com/loongson-gz/ls1b-linux-3.18  
* https://github.com/fxjfsy/pmon-loongsonclub  
* https://github.com/tupelo-shen/my_test/blob/master/doc/linux/mips-architecture/loongson-datasheet/pmon/pmon理解1-start.S文件分析.md  
* https://github.com/mixiaolei007/-/blob/master/applications/main.c  
* https://github.com/loongson-community/pmon  
* https://github.com/loongson/qemu  
* https://github.com/poorjobless/cpu_gs232  
* https://www.douban.com/note/186223156/  
* https://github.com/michaekang/skyeye-testsuite/tree/master/dyncom/hello_gs32eb1  

## mips, nscscc  
* https://github.com/nscscc2019ucas/nscscc2019ucas/blob/master/display/soc_up/simu/soft/func/test.lds  
* https://github.com/lxfei7310/nontrivial-mips/tree/master/loongson/soc_run_os/simu/soft/func  
* https://github.com/leliyliu/augmips/blob/master/nscscc2019_release_v0.01/soc_run_os_v0.01/soc_up/simu/soft/func/start.S  
* https://github.com/imhcyx/nscscc-pmon    
* https://github.com/easter-mips/nscscc2020  

## mips r3000 os  
* search linker script, Written by Martin Mares  
* https://github.com/roife/BUAA-OS  
* https://github.com/BXYMartin/MIPS-OS  
* https://github.com/cqd123123/operating_system  
* https://github.com/sinoyou/BUAA_Operating_System  
* https://github.com/Amadeus979/lab6_learn  
* https://github.com/gitccl/BUAA-OSLAB-2020  
* https://github.com/SivilTaram/Jos-mips  
* https://github.com/yiliangw/CourseProject-MipsJOS  
* https://github.com/TaoFu-0204/BUAA-OS-2021-RISC-V  
* https://github.com/zyy0721/Minisys-OS  
* https://github.com/Niupple/BUAA-OS-Niupple  
* search mips r3000  
* search buaa os  

## os161, sys161, mips r2000/r3000, for mipseb, idt30xx    
* http://www.os161.org  
* https://github.com/ops-class/os161  
* https://student.cs.uwaterloo.ca/~cs350/common/Install161NonCS.html  
* https://student.cs.uwaterloo.ca/~cs350/common/Install161.html  
* https://github.com/Uberi/uw-cs350-development-environment  
* https://cgi.cse.unsw.edu.au/~cs3231/os161/index.php  
* https://cgi.cse.unsw.edu.au/~cs3231/doc/R3000.pdf  

## (TODO) 数字设计和计算机体系结构  
* https://booksite.elsevier.com/9780123944245/  
* https://www.elsevier.com/books/digital-design-and-computer-architecture/harris/978-0-12-394424-5  
* (IMP) DDCA_Labs_companion.zip, mipstop.sv, DE2  
* (IMP) DDCA2e_HDL_03-11-2015.zip, 07-mipssingle.sv    
