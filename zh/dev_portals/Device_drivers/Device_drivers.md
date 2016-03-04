> 原文：: [eLinux.org](http://eLinux.org/Device_drivers "http://eLinux.org/Device_drivers")<br/>
> 翻译：[@EmbolismSoil](https://github.com/EmbolismSoil)<br/>

# 设备驱动



## 手册

-   [Linux内核内部参考手册,
    wikibook](http://en.wikibooks.org/wiki/The_Linux_Kernel) - 正在完善中
-   [Linux设备驱动, 第三版](http://www.makelinux.net/ldd3/)
-   [并口驱动程序开发教程](http://www.makelinux.net/reference.d/drivers_linux)

## 示例驱动

-   [LDT - Linux驱动程序模板](https://github.com/makelinux/ldt/) -
    用于学习着手定制源码级设备驱动程序的示例模板。作为展示例子，实现了UART字符设备驱动程序. 使用到了以下Linux工具: module, platform driver,
    file operations (read/write, mmap, ioctl, blocking and nonblocking
    mode, polling), kfifo, completion, interrupt, tasklet, work,
    kthread, timer, misc device, proc fs, UART 0x3f8, HW loopback, SW
    loopback, ftracer。此代码在测试脚本下可以正常工作。
-   [LDD3 - 启动Linux设备驱动的示例, 第三版,
    已更新](https://github.com/martinezjavier/ldd3/), 使用3.2.0版本的内核进行编译
    -   [pci\_skel.c](https://github.com/martinezjavier/ldd3/blob/master/pci/pci_skel.c)
        - PCI 驱动程序框架
    -   [sbull.c](https://github.com/martinezjavier/ldd3/blob/master/sbull/sbull.c)
        - 简单的块设备
    -   [scull](https://github.com/martinezjavier/ldd3/tree/master/scull)
        - 简单的字符设备
    -   [snull.c](https://github.com/martinezjavier/ldd3/blob/master/snull/snull.c)
        - 简单的网络设备
-   [vivi.c -
     使用了V4L2的Linux虚拟视频驱动](http://lxr.free-electrons.com/source/drivers/media/video/vivi.c)
    - works
-   [mem2mem\_testdev.c - 虚拟的 v4l2-mem2mem 设备驱动例子
    ](http://lxr.free-electrons.com/source/drivers/media/video/mem2mem_testdev.c)
-   [usb-skeleton.c -
     USB驱动程序框架](http://lxr.free-electrons.com/source/drivers/usb/usb-skeleton.c)
    (经过稍微修改后即可编译通过)
-   [skeletonfb.c - Frame
     Buffer设备驱动框架](http://lxr.free-electrons.com/source/drivers/video/skeletonfb.c)
    (不能编译通过)
-   [pcihp\_skeleton.c -
     PCI热插拔控制器驱动程序框架](http://lxr.free-electrons.com/source/drivers/pci/hotplug/pcihp_skeleton.c)
-   [loopback.c - 一个简单的网络设备驱动程序，实现了ifconfig
     lo](http://lxr.free-electrons.com/source/drivers/net/loopback.c)
-   [gpio\_driver - Raspberry Pi model
     B+的GPIO设备驱动程序简单示例](https://github.com/23ars/linux_gpio_driver) (尚未进行完整的测试)

## 资源

-   [Device Tree](../../dev_portals/Device_Tree/Device_Tree.md "Device Tree") - 设备树的相关信息 (为了满足日益增加的新嵌入式设备驱动的需求)
