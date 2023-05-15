## Openwrt for GL.iNET ST1200/SFT1200 ##

=====編譯方法======

#進入openwrt-18.06目錄

cd openwrt-18.06

#更新feed

/scripts/feeds update -a && ./scripts/feeds install -a

#編譯SF120

cp .config.sf1200 .config

#編譯SFT1200

cp .config.sf1200 .config

配置所需app

make menuconfig

#編譯

make -j8 download && make V=s -j$(nproc)
