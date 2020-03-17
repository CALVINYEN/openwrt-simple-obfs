Simple-obfs for OpenWrt
===

编译
---

 - 从 OpenWrt 的 [SDK][S] 编译

   ```bash
   # xiaoMi router 3G 设备为例, MTK mt7621
   wget https://downloads.openwrt.org/releases/19.07.2/targets/ramips/mt7621/openwrt-sdk-19.07.2-ramips-mt7621_gcc-7.5.0_musl.Linux-x86_64.tar.xz
   xz -d openwrt-sdk-19.07.2-ramips-mt7621_gcc-7.5.0_musl.Linux-x86_64.tar.xz && tar vxf openwrt-sdk-19.07.2-ramips-mt7621_gcc-7.5.0_musl.Linux-x86_64.tar
   # 添加 feeds
   git clone https://github.com/shadowsocks/openwrt-feeds.git package/feeds
   # 获取 simple-obfs Makefile
   git clone https://github.com/aa65535/openwrt-simple-obfs.git package/simple-obfs
   # 选择要编译的包 Network -> simple-obfs
   make menuconfig
   # 开始编译
   make package/simple-obfs/compile V=99
   ```


  [S]: https://wiki.openwrt.org/doc/howto/obtain.firmware.sdk
